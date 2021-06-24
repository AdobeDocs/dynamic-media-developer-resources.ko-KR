---
description: 레이어 이미지.
solution: Experience Manager
title: src
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 88b89e70-59cf-4fb9-bbe7-0ac5eff792f1
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 3%

---

# src{#src}

레이어 이미지.

` src= *``*|{[is|ir|fxg]'{' *`objectnestedRequest`*'}'}`

<table id="simpletable_59104309B8284B21ABCE7DC95BF5A273"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 개체 </span> </p> </td> 
  <td class="stentry"> <p>이미지 개체. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> nestedRequest  </span> </p> </td> 
  <td class="stentry"> <p>중첩 이미지 제공, 이미지 렌더링 또는 외부 요청. </p> </td> 
 </tr> 
</table>

## 설명 {#section-59ec6dc2afcb43efb34dbb0f7733543f}

이미지 레이어의 소스 이미지를 지정합니다.

*`object`* 카탈로그 항목 또는 이미지/SVG 파일일 수 있습니다.

[개체](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)를 참조하십시오.

중첩된 요청이나 포함된 요청은 중괄호로 묶입니다. 포함된 이미지 제공 요청의 접두사로 `is`, 포함된 이미지 렌더링 요청을 `ir` 로 지정하고, `fxg` 로 FXG 그래픽 렌더링 요청을 사용합니다. 접두사가 지정되지 않은 경우 외부 서버에 대한 요청은 가정됩니다.

[요청 중첩 및 포함](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)을 참조하십시오.

## 속성 {#section-2c22bb89a35d470f833df8ba898efd93}

레이어 속성입니다. `layer=comp`인 경우 `layer=0`에 적용됩니다. 동일한 계층에서 `text=` 및 `textPs=`과 함께 사용할 수 없습니다.`text=`, `textPs=` 또는 `src=`의 마지막 항목 값이 적용되며, 이 항목이 이미지인지 아니면 텍스트 레이어인지 결정합니다. 효과 레이어에서 무시됨.

*`object`*는 `catalog::Modifier`에 `src=` 또는 `mask=` 명령을 포함하는 다른 카탈로그 레코드로 확인할 수 없습니다. (비슷한 효과를 얻으려면 요청 중첩을 사용합니다.)

`is`, `ir` 및 `fxg` 접두사는 대/소문자를 구분합니다.

## 기본값 {#section-a92f3882041b4d43ae2caf014647165f}

레이어 0의 경우 `src=` 이 지정되지 않은 경우 URL의 경로 구성 요소의 개체가 사용됩니다. 다른 레이어의 기본값은 없습니다.

## 참조 {#section-e467e03330564796932ac081f1c9c1d0}

[카탈로그::Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) ,  [속성::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494),  [text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f),  [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767),  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e),  [object](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0),  [템플릿](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e),  [요청 중첩 및 포함](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
