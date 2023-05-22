---
description: 명령 매크로는 명령 집합에 대해 명명된 단축키를 제공합니다. 매크로는 이미지 카탈로그나 기본 카탈로그에 첨부할 수 있는 별도의 매크로 정의 파일로 정의됩니다.
solution: Experience Manager
title: 명령 매크로
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 304d93af-3427-4111-882a-35be9ec3aef5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 1%

---

# 명령 매크로{#command-macros}

명령 매크로는 명령 집합에 대해 명명된 단축키를 제공합니다. 매크로는 이미지 카탈로그나 기본 카탈로그에 첨부할 수 있는 별도의 매크로 정의 파일로 정의됩니다.

`$ *`name`*$`

<table id="simpletable_A03541622C354F60B5F304B999C4EF8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 이름</span></span> </p> </td> 
  <td class="stentry"> <p>매크로 이름. </p></td> 
 </tr> 
</table>

`*`이름`*` 는 대/소문자를 구분하지 않으며 ASCII 문자, 숫자 , &#39;-&#39;, &#39;_&#39; 및 &#39;.&#39;의 조합으로 구성될 수 있습니다. 문자.

매크로는 요청의 어디에서나 &#39;?&#39; 뒤에 호출할 수 있고 `catalog::Modifier` 또는 `catalog::PostModifier` 필드. 매크로는 하나 이상의 완전한 이미지 제공 명령만 나타낼 수 있으며 &#39;&amp;&#39; 구분 기호를 사용하여 다른 명령과 구분해야 합니다.

매크로 호출은 구문 분석 중에 대체 문자열로 조기에 대체됩니다. 매크로 내의 명령은 요청에서 매크로 호출 전에 발생할 경우 요청에서 동일한 명령을 재정의합니다. 이 은(는) 과(와) 다릅니다. `catalog::Modifier`: 요청 문자열의 명령이 항상 의 명령을 재정의합니다. `catalog::Modifier` 문자열(요청에서 위치에 상관없이).

명령 매크로에는 인수 값을 사용할 수 없지만 사용자 지정 변수를 사용하여 요청에서 매크로로 값을 전달할 수 있습니다.

매크로는 다음 제한 사항을 사용하여 중첩될 수 있습니다. 매크로 정의를 구문 분석할 때 동일한 매크로 정의 파일에서 앞에 나타나거나 기본 매크로 정의 파일에 포함된 매크로에 대한 정의를 배치하는 방식으로 매크로가 이미 정의된 경우에만 매크로를 호출할 수 있습니다.

## 예 {#section-2f73d36ac8d64254a03bae5afeae2fb9}

매크로는 동일한 특성을 다른 이미지에 적용할 경우에 유용합니다.

`http://server/cat/1345?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/1435?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/8243?wid=480&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

공통 속성에 대한 매크로를 정의할 수 있습니다.

`view wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

매크로는 다음과 같이 사용됩니다.

`http://server/cat/1345?$view$ http://server/cat/1435?$view$ http://server/cat/8243?$view$&wid=480`

다음 이후 `wid=` 은 세 번째 요청에 대해 다르므로 값을 재정의합니다. *이후* 매크로가 호출됩니다(지정) `wid=`*다음 이전* `$view$` 에는 영향이 없습니다).

## 참조 {#section-8cdba0ed2480444ca61e719e54f8871c}

[catalog::MacroFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-macrofile.md#reference-f91d717b3847458ca0f1fe95387554a2) , [catalog::Modifier](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md), [매크로 정의 참조](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-macro-definition-reference/c-macro-definition-reference.md#concept-5ec73f7636c1496fba1e94094e694e79)
