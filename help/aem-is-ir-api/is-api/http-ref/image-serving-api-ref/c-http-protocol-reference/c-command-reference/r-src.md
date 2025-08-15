---
title: src
description: 레이어 이미지.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 88b89e70-59cf-4fb9-bbe7-0ac5eff792f1
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 2%

---

# src{#src}

레이어 이미지.

` src= *`개체`*|{[is|ir|fxg]'{' *`nestedRequest`*'}'}`

<table id="simpletable_59104309B8284B21ABCE7DC95BF5A273"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 개체 </span> </p> </td> 
  <td class="stentry"> <p>이미지 개체입니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> nestedRequest </span> </p> </td> 
  <td class="stentry"> <p>중첩 이미지 제공, 이미지 렌더링 또는 외부 요청. </p> </td> 
 </tr> 
</table>

## 설명 {#section-59ec6dc2afcb43efb34dbb0f7733543f}

이미지 레이어의 소스 이미지를 지정합니다.

*`object`*&#x200B;은(는) 카탈로그 항목 또는 이미지/SVG 파일일 수 있습니다.

[개체](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)를 참조하십시오.

중첩된 요청이나 포함된 요청은 중괄호로 묶입니다. `is`이(가) 포함된 이미지 제공 요청, `ir`이(가) 포함된 이미지 렌더링 요청 및 `fxg`이(가) 포함된 FXG 그래픽 렌더링 요청 접두사로 사용됩니다. 접두사가 지정되지 않은 경우 외부 서버 요청이 가정됩니다.

[중첩 및 포함 요청](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)을 참조하십시오.

## 속성 {#section-2c22bb89a35d470f833df8ba898efd93}

레이어 속성입니다. `layer=0`인 경우 `layer=comp`에 적용됩니다. 같은 레이어에서 `text=` 및 `textPs=`과(와) 함께 사용할 수 없습니다. `text=`, `textPs=` 또는 `src=`의 마지막 항목이 우세하여 이것이 이미지 레이어인지 텍스트 레이어인지를 결정합니다. 효과 레이어에서 무시됨.

*`object`*은(는) 해당 `src=`에 `mask=` 또는 `catalog::Modifier` 명령을 포함하는 다른 카탈로그 레코드로 확인할 수 없습니다. (요청 중첩을 사용하여 유사한 효과를 얻을 수 있습니다.)

`is`, `ir` 및 `fxg` 접두사는 대/소문자를 구분합니다.

## 기본값 {#section-a92f3882041b4d43ae2caf014647165f}

`src=`이(가) 지정되지 않은 경우 레이어 0의 경우 URL의 경로 구성 요소에 있는 개체가 사용됩니다. 다른 레이어의 기본값은 없습니다.

## 참조 {#section-e467e03330564796932ac081f1c9c1d0}

[카탈로그::경로](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) , [특성::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494), [텍스트=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f), [텍스트Ps=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767), [마스크=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [개체](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0), [템플릿](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [중첩 및 포함 요청](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
