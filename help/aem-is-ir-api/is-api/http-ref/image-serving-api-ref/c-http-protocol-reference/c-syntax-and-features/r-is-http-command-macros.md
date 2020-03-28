---
description: 명령 매크로는 명령 세트에 대해 명명된 단축키를 제공합니다. 매크로는 이미지 카탈로그 또는 기본 카탈로그에 첨부할 수 있는 별도의 매크로 정의 파일에 정의됩니다.
seo-description: 명령 매크로는 명령 세트에 대해 명명된 단축키를 제공합니다. 매크로는 이미지 카탈로그 또는 기본 카탈로그에 첨부할 수 있는 별도의 매크로 정의 파일에 정의됩니다.
seo-title: 명령 매크로
solution: Experience Manager
title: 명령 매크로
topic: Scene7 Image Serving - Image Rendering API
uuid: a6ff5642-6716-484f-b37e-066994362a9b
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150

---


# 명령 매크로{#command-macros}

명령 매크로는 명령 세트에 대해 명명된 단축키를 제공합니다. 매크로는 이미지 카탈로그 또는 기본 카탈로그에 첨부할 수 있는 별도의 매크로 정의 파일에 정의됩니다.

`$ *`name`*$`

<table id="simpletable_A03541622C354F60B5F304B999C4EF8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 이름</span></span> </p> </td> 
  <td class="stentry"> <p>매크로 이름. </p></td> 
 </tr> 
</table>

` *`name`*` is not case-sensitive and may conduct of any combination of ASCII letters, number, &#39;-&#39;, &#39;_&#39; 및 &#39;&#39;. 문자.

매크로는 &#39;?&#39; 이후의 요청에서 `catalog::Modifier` 또는 `catalog::PostModifier` 필드 내의 어느 위치에서나 호출할 수 있습니다. 매크로는 하나 이상의 완전한 이미지 제공 명령만 나타낼 수 있으며 &#39;&amp;&#39; 구분 기호가 있는 다른 명령과 구분해야 합니다.

구문 분석 중에는 일찍 매크로 함수가 대체 문자열로 대체됩니다. 매크로 내의 명령은 요청에서 매크로 호출 전에 발생하는 경우 요청에서 동일한 명령을 덮어씁니다. 이것은 `catalog::Modifier`요청에서 위치에 관계없이 요청 문자열의 명령은 항상 `catalog::Modifier` 문자열의 명령을 재정의합니다.

명령 매크로에는 인수 값을 사용할 수 없지만 사용자 지정 변수를 사용하여 요청의 값을 매크로로 전달할 수 있습니다.

매크로가 중첩될 수 있으며 다음과 같은 제한이 있습니다.매크로를 호출할 수 있는 경우는 매크로 정의가 구문 분석될 때, 같은 매크로 정의 파일에 앞에 표시되거나 기본 매크로 정의 파일에 포함된 매크로의 정의를 삽입하여 매크로 정의를 찾을 수 있습니다.

## 예 {#section-2f73d36ac8d64254a03bae5afeae2fb9}

매크로는 동일한 속성을 다른 이미지에 적용할 때 유용합니다.

`http://server/cat/1345?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/1435?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/8243?wid=480&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

일반적인 속성에 대한 매크로를 정의할 수 있습니다.

`view wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

매크로는 다음과 같이 사용됩니다.

`http://server/cat/1345?$view$ http://server/cat/1435?$view$ http://server/cat/8243?$view$&wid=480`

세 번째 요청에 `wid=` 대해 다르므로, 매크로 호출 *후* 값을 재정의하면 `wid=`*아무 영향도&#x200B;*`$view$`없을 수 있습니다.

## 참조 {#section-8cdba0ed2480444ca61e719e54f8871c}

[catalog::MacroFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-macrofile.md#reference-f91d717b3847458ca0f1fe95387554a2) , [catalog::Modifier](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md), [Macro Definition Reference](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-macro-definition-reference/c-macro-definition-reference.md#concept-5ec73f7636c1496fba1e94094e694e79)
