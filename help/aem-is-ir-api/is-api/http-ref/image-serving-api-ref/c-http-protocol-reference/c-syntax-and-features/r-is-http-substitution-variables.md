---
description: 대체 변수는 요청 URL에서 이미지 카탈로그에 저장된 합성 템플릿으로 값을 전송하는 데 사용됩니다. 변수를 사용하여 복잡한 요청의 다른 위치에 동일한 값을 전달할 수도 있습니다.
seo-description: 대체 변수는 요청 URL에서 이미지 카탈로그에 저장된 합성 템플릿으로 값을 전송하는 데 사용됩니다. 변수를 사용하여 복잡한 요청의 다른 위치에 동일한 값을 전달할 수도 있습니다.
seo-title: 대체 변수
solution: Experience Manager
title: 대체 변수
topic: Scene7 Image Serving - Image Rendering API
uuid: e369f2c3-8d89-4169-8869-f1d7ab89aab9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 0%

---


# 대체 변수{#substitution-variables}

대체 변수는 요청 URL에서 이미지 카탈로그에 저장된 합성 템플릿으로 값을 전송하는 데 사용됩니다. 변수를 사용하여 복잡한 요청의 다른 위치에 동일한 값을 전달할 수도 있습니다.

` $ *``*= *`varvalue`*`

<table id="simpletable_EFEC66C23CE949EFACDC415A954DF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var  </span> </span> </p> </td> 
  <td class="stentry"> <p>변수 이름. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
  <td class="stentry"> <p>변수를 설정할 값(문자열)입니다. </p> </td> 
 </tr> 
</table>

변수 정의 및 참조는 요청의 쿼리 부분, `catalog::Modifier` 및 `catalog::PostModifier`에서 발생할 수 있습니다.

변수는 다른 IS 명령과 유사하게 위와 같이 정의됩니다.행간 &#39;$&#39;은(는) 명령을 변수 정의로 식별합니다. 변수는 참조하기 전에 정의해야 합니다.

변수 이름 *`var`*&#x200B;은 대/소문자를 구분하지 않으며 ASCII 문자, 숫자, &#39;-&#39;, &#39;_&#39; 및 &#39;.&#39;의 조합으로 구성될 수 있습니다.

>[!NOTE]
>
>*`value`* 안전한 HTTP 전송을 위해 단일 패스 URL로 인코딩되어야 합니다. *`value`*&#x200B;이(가) HTTP를 통해 다시 전송되는 경우 이중 인코딩이 필요합니다. 이 경우 *`value`*&#x200B;이(가) 중첩 외부 요청으로 대체되거나 SVG `<image>` 요소의 href 특성으로 대체됩니다.

변수 참조는 선행 및 후행 &#39;$&#39;($*var*$)로 구분된 변수 이름으로 구성됩니다. 참조는 모든 IS 명령의 값 부분(즉, 명령 이름 뒤에 오는 &#39;=&#39; 사이 또는 그 뒤의 &#39;&amp;&#39; 사이 또는 요청의 끝) 어디에서든 발생할 수 있습니다. 사용자 지정 변수는 `layer=` 및 `effect=` 명령에 적용할 수 없습니다. 동일한 명령 값에 여러 변수가 허용됩니다. 서버는 각 ` $ *`var`*$`의 발생을 *`value`*&#x200B;로 대체합니다.

변수 참조는 중첩될 수 없습니다. *`value`* 내에 ` $ *`var`*$`이 있는 모든 항목은 대체되지 않습니다.

예를 들어 요청 조각:

`$var2=apple&$var1=my$var2$tree&text=$var1$`

해결 방법:

`text=my$var2$tree`

>[!NOTE]
>
>&#39;$&#39;은(는) 예약된 문자가 아닙니다.이 문제는 요청에서 다르게 발생할 수 있습니다. 예를 들어 `wid`에는 숫자 인수가 필요하므로 `src=my$image$file.tif`은(는) 유효한 명령(이름이 `my$image$file.tif`인 카탈로그 항목 또는 이미지 파일이 있다고 가정할 때), `wid=$number$`은(는) 존재하지 않습니다.

## 중첩된 요청의 변수 처리 {#section-26d63adc446c4fa0808e11e8082abdfa}

` $ *`&#39;?&#39; `*$` 왼쪽에 포함하여 중첩된 이미지 제공 또는 이미지 렌더링 요청의 중괄호 안의 모든 위치에서 변수 참조가 발생할 수 있습니다. 쿼리와 경로 구분. 서버는 중첩된 요청의 추가 구문 분석 및 처리를 전에 이러한 참조를 값(URL 또는 기본 이미지 카탈로그의 `catalog::Modifier`)으로 대체합니다.

또한 URL 또는 `catalog::Modifier`의 모든 ` $ *`var`*=` 정의는 모든 중첩된 이미지 제공 및 이미지 렌더링 요청에 전달됩니다. 이렇게 하면 중첩 수준에 관계없이 모든 변수 정의를 모든 템플릿에 사용할 수 있습니다.

중첩 수준에 관계없이, 중첩된 이미지 렌더링 또는 이미지 제공 요청이나 관련 `catalog::Modifier` 문자열의 어느 위치로든 대체될 변수 값에 단일 패스 HTTP 인코딩만 적용해야 합니다.

## 포함된 외부 요청의 변수 처리 {#section-314e39a9aefb46faa737fd137897d1b0}

` $ *`임베드된 `*$` 외래 요청의 중괄호 안에서 발생하는 varreferences는 일치하는 변수 정의 값으로 대체됩니다. 이를 통해 임베드된 외부 요청을 이미지 카탈로그의 템플릿에 배치할 수 있습니다.

서버가 최종 외래 URL을 전송하려고 시도하기 전에 다시 인코딩이 적용되지 않으므로 일반적으로 외부 요청으로 대체될 변수 값은 이중 인코딩되어야 합니다.

## SVG 파일 {#section-a8359f9909764142b6a18ae778dca913}의 변수 처리

` $ *`변수 참조`*$` 는 특성 값 및 문자열의 SVG 파일에서 발생할 수  `<text>` 있습니다. 이미지 제공은 SVG 파일이 지정된 요청 중첩 수준에서 알려진 일치하는 ` $ *`var`*=` 정의로 대체합니다.

>[!NOTE]
>
>`href` 속성 값으로 대체될 모든 변수 값은 이중 URL 인코딩되어야 합니다.다른 모든 항목은 단일 인코딩으로 인코딩되어야 합니다.

## 사전 정의된 경로 변수 {#section-930d0dd12e8f49499becc9fe8df24092}

요청 경로에 지정된 *`object`*&#x200B;은 사전 정의된 변수 ` *`$object`*`에 할당됩니다. &#39; ` $ *`object`*$`&#39;는 요청에서 참조한 템플릿 또는 `src=` 및 `mask=` 값과 중첩/포함된 요청의 경로를 포함하여 해당 개체가 허용되는 중첩/포함된 요청에서 요청의 어느 곳에나 배치할 수 있습니다.

예를 들어, 다음 요청은 경로에 지정된 이미지를 중첩 요청에서 레이어의 소스로 재사용합니다.

`/is/image/a/b?…&layer=3&src=is{…&src=$object$}&…`

이것은

`/is/image/a/b?…&layer=3&src=is{…&src=a/b}&…`

` *`$object`*`의 정의는 원하는 값으로 ` $ *`object`*=`을 명시적으로 지정하여 재정의할 수 있습니다.

사전 정의된 경로 변수는 일반적으로 `template=`과 함께 사용됩니다.

## 기본값 {#section-b02483d15529444586a2e9504805b155}

없음. 정의된 변수만 서버에 의해 대체됩니다(사전 정의된 경로 변수 $object 제외(항상 대체됨). ` *`var`*`이(가) 기존 변수 정의와 일치할 수 없는 경우 ` $ *`var`*$`의 모든 항목은 리터럴로 유지됩니다.

## 예제 {#section-fba9393df6984247b7e30b3f93992e86}

[템플릿](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)의 &quot;예 A&quot;를 참조하십시오.

## 참조 {#section-11b44cc824744f70b1705ebdd9ec4fe6}

[템플릿](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e),  [template=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-template.md#reference-3beccaa462a64bf0ba867e5c8fd0bd14)
