---
description: 대체 변수는 요청 URL에서 이미지 카탈로그에 저장된 작성 템플릿으로 값을 전송하는 데 사용됩니다. 변수를 사용하여 복잡한 요청의 다른 위치에 동일한 값을 전달할 수도 있습니다.
solution: Experience Manager
title: 대체 변수
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9fd73d16-e8bd-4fdb-a4e6-e86e5d219114
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '729'
ht-degree: 0%

---

# 대체 변수{#substitution-variables}

대체 변수는 요청 URL에서 이미지 카탈로그에 저장된 작성 템플릿으로 값을 전송하는 데 사용됩니다. 변수를 사용하여 복잡한 요청의 다른 위치에 동일한 값을 전달할 수도 있습니다.

` $ *`var`*= *`value`*`

<table id="simpletable_EFEC66C23CE949EFACDC415A954DF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var </span> </span> </p> </td> 
  <td class="stentry"> <p>변수 이름. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value </span> </span> </p> </td> 
  <td class="stentry"> <p>변수를 설정할 값(문자열)입니다. </p> </td> 
 </tr> 
</table>

변수 정의 및 참조는 요청의 쿼리 부분에서 발생할 수 있습니다. `catalog::Modifier`, 및 `catalog::PostModifier`.

변수는 다른 IS 명령과 유사하며 위와 같이 정의됩니다. 선행 &#39;$&#39;은(는) 명령을 변수 정의로 식별합니다. 변수를 참조하기 전에 정의해야 합니다.

변수 이름 *`var`* 는 대/소문자를 구분하지 않으며 ASCII 문자, 숫자, &#39;-&#39;, &#39;_&#39; 및 &#39;&#39;의 조합으로 구성될 수 있습니다.

>[!NOTE]
>
>*`value`* 안전한 HTTP 전송을 위해 단일 전달 URL로 인코딩되어야 합니다. 이중 인코딩이 필요한 경우 *`value`* 는 HTTP를 통해 다시 전송됩니다. 이 경우 *`value`* 는 중첩된 외부 요청 또는 SVG의 href 특성으로 대체됩니다 `<image>` 요소를 생성하지 않습니다.

변수 참조는 선행 및 후행 &#39;$&#39;($$)로 구분된 변수 이름으로 구성됩니다&#x200B;*var*$). IS 명령의 값 부분(즉, 명령 이름과 후속 &#39;&amp;&#39; 또는 요청 끝 뒤에 오는 &#39;=&#39; 사이)의 어느 곳에서든 참조가 발생할 수 있습니다. 사용자 지정 변수는 `layer=` 및 `effect=` 명령. 동일한 명령 값에는 여러 변수가 허용됩니다. 서버는 ` $ *`var`*$` with *`value`*.

변수 참조는 중첩되지 않을 수 있습니다. 모든 발생 횟수 ` $ *`var`*$` within *`value`* 은 대체되지 않습니다.

예를 들어 요청 조각은

`$var2=apple&$var1=my$var2$tree&text=$var1$`

해결 방법:

`text=my$var2$tree`

>[!NOTE]
>
>&#39;$&#39;은(는) 예약된 문자가 아닙니다. 이 문제는 요청에서 달리 발생할 수 있습니다. 예, `src=my$image$file.tif` 는 유효한 명령입니다(카탈로그 항목 또는 이미지 파일이 `my$image$file.tif` 존재) `wid=$number$` 아님 `wid` 에는 숫자 인수가 필요합니다.

## 중첩 요청의 변수 처리 {#section-26d63adc446c4fa0808e11e8082abdfa}

` $ *`var`*$` 참조는 &#39;?&#39; 왼쪽의 를 포함하여 중첩된 이미지 제공 또는 이미지 렌더링 요청의 중괄호 내 어디에서든 발생할 수 있습니다 쿼리에서 경로 구분 서버는 이러한 참조를 URL의 값 또는 `catalog::Modifier` 중첩된 요청의 추가 구문 분석 및 처리 전에 기본 이미지 카탈로그의 매개 변수를 검토하십시오.

게다가, ` $ *`var`*=` url 또는 `catalog::Modifier` 모든 중첩 이미지 제공 및 이미지 렌더링 요청으로 전달됩니다. 이렇게 하면 중첩 수준에 관계없이 모든 템플릿에서 모든 변수 정의를 사용할 수 있습니다.

중첩 수준에 관계없이, 중첩 이미지 렌더링 또는 이미지 제공 요청의 어느 곳에서든 대체될 변수 값이나 연결된 변수에는 단일 패스 HTTP 인코딩만 적용되어야 합니다 `catalog::Modifier` 문자열.

## 포함된 외부 요청의 변수 처리 {#section-314e39a9aefb46faa737fd137897d1b0}

` $ *`var`*$` 포함된 외부 요청의 중괄호 내에서 발생하는 참조는 일치하는 변수 정의 값으로 대체됩니다. 이를 통해 포함된 외부 요청을 이미지 카탈로그의 템플릿에 배치할 수 있습니다.

서버가 최종 외부 URL을 전송하려고 하기 전에 재인코딩이 적용되지 않으므로 일반적으로 외부 요청으로 대체될 변수 값은 이중 인코딩해야 합니다.

## SVG 파일의 변수 처리 {#section-a8359f9909764142b6a18ae778dca913}

` $ *`var`*$` 참조는 속성 값의 SVG 파일에서 `<text>` 문자열. 이미지 제공 서비스는 이 매개 변수들을 일치하는 항목으로 대체합니다 ` $ *`var`*=` SVG 파일이 지정된 요청 중첩 수준에서 알려진 정의입니다.

>[!NOTE]
>
>로 대체될 모든 변수 값 `href` 특성 값은 이중 URL로 인코딩되어야 합니다. 다른 모든 항목은 단독으로 인코딩되어야 합니다.

## 사전 정의된 경로 변수 {#section-930d0dd12e8f49499becc9fe8df24092}

다음 *`object`* 요청 경로에 지정되는 변수가 미리 정의된 변수에 할당됩니다 `*`$object`*`. ` ` $ *`개체`*$`&#39;은(는) 요청의 어느 곳에서든, 요청에 의해 참조되는 템플릿이나, 해당 개체가 허용되는 중첩/포함된 요청에서 배치할 수 있습니다(값 포함). `src=` 및 `mask=`, 중첩된/포함된 요청의 경로.

예를 들어 다음 요청은 경로에 지정된 이미지를 중첩 요청에 있는 레이어의 소스로 재사용합니다.

`/is/image/a/b?…&layer=3&src=is{…&src=$object$}&…`

이것은 다음과 같습니다

`/is/image/a/b?…&layer=3&src=is{…&src=a/b}&…`

의 정의 `*`$object`*` 을 명시적으로 지정하여 재정의할 수 있습니다. ` $ *`개체`*=` 원하는 값으로 변경하려는 경우.

사전 정의된 경로 변수는 일반적으로 `template=`.

## 기본값 {#section-b02483d15529444586a2e9504805b155}

없음. 정의된 변수만 서버에 의해 대체됩니다(항상 대체되는 사전 정의된 경로 변수 $object 제외). 모든 발생 횟수 ` $ *`var`*$` 다음의 경우 리터럴 `*`var`*`기존 변수 정의와 일치할 수 없습니다.

## 예제 {#section-fba9393df6984247b7e30b3f93992e86}

의 &quot;예제 A&quot;를 참조하십시오. [템플릿](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## 참조 {#section-11b44cc824744f70b1705ebdd9ec4fe6}

[템플릿](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [template=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-template.md#reference-3beccaa462a64bf0ba867e5c8fd0bd14)
