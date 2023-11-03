---
description: 대체 변수는 요청 URL의 값을 이미지 카탈로그에 저장된 조합 템플릿으로 전송하는 데 사용됩니다. 변수를 사용하여 복잡한 요청의 여러 위치에 동일한 값을 전달할 수도 있습니다.
solution: Experience Manager
title: 대체 변수
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9fd73d16-e8bd-4fdb-a4e6-e86e5d219114
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 0%

---

# 대체 변수{#substitution-variables}

대체 변수는 요청 URL의 값을 이미지 카탈로그에 저장된 조합 템플릿으로 전송하는 데 사용됩니다. 변수를 사용하여 복잡한 요청의 여러 위치에 동일한 값을 전달할 수도 있습니다.

` $ *`var`*= *`값`*`

<table id="simpletable_EFEC66C23CE949EFACDC415A954DF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var </span> </span> </p> </td> 
  <td class="stentry"> <p>변수 이름. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 값 </span> </span> </p> </td> 
  <td class="stentry"> <p>변수를 설정할 값(문자열). </p> </td> 
 </tr> 
</table>

변수 정의 및 참조는 요청의 쿼리 부분에서 발생할 수 있습니다. `catalog::Modifier`, 및 `catalog::PostModifier`.

변수는 다른 IS 명령과 마찬가지로 위와 같이 정의됩니다. 선행 &#39;$&#39;는 명령을 변수 정의로 식별합니다. 변수를 참조하기 전에 정의해야 합니다.

변수 이름 *`var`* 는 대/소문자를 구분하지 않으며 ASCII 문자, 숫자, &#39;-&#39;, &#39;_&#39; 및 &#39;.&#39;의 조합으로 구성될 수 있습니다.

>[!NOTE]
>
>*`value`* 안전한 HTTP 전송을 위해 단일 패스 URL로 인코딩해야 합니다. 다음의 경우 이중 인코딩이 필요합니다. *`value`* 은 HTTP를 통해 재전송됩니다. 이 경우는 다음과 같습니다 *`value`* 는 중첩된 외부 요청 또는 SVG의 href 특성으로 대체됩니다. `<image>` 요소를 생성하지 않습니다.

변수 참조는 선행 및 후행 &#39;$&#39;($)로 구분된 변수 이름으로 구성됩니다.*var*$). 참조는 모든 IS 명령의 값 부분(즉, 명령 이름 다음에 오는 &#39;=&#39;와 후속 &#39;&amp;&#39; 사이 또는 요청 끝) 어디에서든 발생할 수 있습니다. 사용자 지정 변수는 `layer=` 및 `effect=` 명령입니다. 동일한 명령 값에는 여러 변수를 사용할 수 있습니다. 서버는 다음의 각 발생으로 대체합니다. ` $ *`var`*$` 포함 *`value`*.

변수 참조는 중첩될 수 없습니다. 다음 중 발생 횟수 ` $ *`var`*$` 다음 범위 내 *`value`* 은 대체되지 않습니다.

예를 들어 요청 조각:

`$var2=apple&$var1=my$var2$tree&text=$var1$`

은(는) 다음을 확인합니다.

`text=my$var2$tree`

>[!NOTE]
>
>&#39;$&#39;은(는) 예약된 문자가 아닙니다. 요청에서 다른 문자가 발생할 수 있습니다. 예를 들어, `src=my$image$file.tif` 은(는) 유효한 명령입니다( 라는 카탈로그 항목 또는 이미지 파일이 있다고 가정). `my$image$file.tif` 존재함), while `wid=$number$` 은(는) 다음과 같지 않습니다. `wid` 에는 숫자 인수가 필요합니다.

## 중첩된 요청에서 변수 처리 {#section-26d63adc446c4fa0808e11e8082abdfa}

` $ *`var`*$` &#39;?&#39; 왼쪽을 포함하여 중첩된 이미지 제공 또는 이미지 렌더링 요청의 중괄호 내 아무 곳에나 참조가 발생할 수 있습니다. 쿼리에서 경로 구분. 서버는 이러한 참조를 다음 값(url 또는 `catalog::Modifier` 중첩된 요청의 추가 구문 분석 및 처리 전 기본 이미지 카탈로그의 참조).

또한, 모두 ` $ *`var`*=` url 또는 `catalog::Modifier` 모든 중첩 이미지 제공 및 이미지 렌더링 요청으로 전달됩니다. 이렇게 하면 중첩 수준에 관계없이 모든 템플릿에서 모든 변수 정의를 사용할 수 있습니다.

중첩 수준에 관계없이, 중첩된 이미지 렌더링 또는 이미지 제공 요청 또는 이와 관련된 모든 위치에서 대체할 변수 값에는 단일 패스 HTTP 인코딩만 적용해야 합니다 `catalog::Modifier` 문자열.

## 포함된 외부 요청에서 변수 처리 {#section-314e39a9aefb46faa737fd137897d1b0}

` $ *`var`*$` 포함된 외부 요청의 중괄호 내에서 발생하는 참조는 일치하는 변수 정의 값으로 대체됩니다. 이렇게 하면 포함된 외부 요청을 이미지 카탈로그의 템플릿에 배치할 수 있습니다.

서버가 최종 외부 URL을 전송하려고 시도하기 전에 다시 인코딩이 적용되지 않으므로 외부 요청으로 대체되는 변수 값은 일반적으로 이중 인코딩이 적용되어야 합니다.

## SVG 파일에서 변수 처리 {#section-a8359f9909764142b6a18ae778dca913}

` $ *`var`*$` 참조는 속성 값 및 의 SVG 파일에서 발생할 수 있습니다. `<text>` 문자열. 이미지 제공에서는 이 값들을 일치하는 것으로 대체합니다 ` $ *`var`*=` SVG 파일이 지정되는 요청 중첩 수준에서 알려진 정의.

>[!NOTE]
>
>로 대체할 모든 변수 값 `href` 속성 값은 이중 URL로 인코딩되어야 하고 다른 모든 값은 단일 인코딩되어야 합니다.

## 사전 정의된 경로 변수 {#section-930d0dd12e8f49499becc9fe8df24092}

다음 *`object`* 요청 경로에 지정된 은(는) 사전 정의된 변수에 할당됩니다. `*`$object`*`. &#39; ` $ *`오브젝트`*$`&#39;는 요청, 요청에서 참조한 템플릿 또는 다음 값을 포함하여 이러한 개체가 허용되는 중첩된/포함된 요청의 어디에나 배치할 수 있습니다. `src=` 및 `mask=`, 중첩/포함된 요청의 경로 등 세 가지 작업을 수행할 수 있습니다.

예를 들어 다음 요청은 경로에 지정된 이미지를 중첩 요청의 레이어 소스로 재사용합니다.

`/is/image/a/b?…&layer=3&src=is{…&src=$object$}&…`

이는 와 동일합니다.

`/is/image/a/b?…&layer=3&src=is{…&src=a/b}&…`

의 정의 `*`$object`*` 명시적으로 지정하여 재정의할 수 있습니다. ` $ *`오브젝트`*=` (원하는 값 포함)

사전 정의된 경로 변수는 일반적으로 `template=`.

## 기본값 {#section-b02483d15529444586a2e9504805b155}

없음. 정의된 변수만 서버에서 대체됩니다(항상 대체되는 사전 정의된 경로 변수 $object 제외). 다음 중 발생 횟수 ` $ *`var`*$` 다음과 같은 경우 리터럴으로 유지 `*`var`*`기존 변수 정의와 일치시킬 수 없습니다.

## 예제 {#section-fba9393df6984247b7e30b3f93992e86}

에서 &quot;예제 A&quot; 참조 [템플릿](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## 참조 {#section-11b44cc824744f70b1705ebdd9ec4fe6}

[템플릿](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [template=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-template.md#reference-3beccaa462a64bf0ba867e5c8fd0bd14)
