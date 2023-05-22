---
description: 레이어 이미지.
solution: Experience Manager
title: src
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 88b89e70-59cf-4fb9-bbe7-0ac5eff792f1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 2%

---

# src{#src}

레이어 이미지.

` src= *`오브젝트`*|{[is|ir|fxg]'{' *`nestedRequest`*'}'}`

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

*`object`* 카탈로그 항목 또는 이미지/SVG 파일일 수 있습니다.

다음을 참조하십시오 [오브젝트](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0).

중첩된 요청이나 포함된 요청은 중괄호로 묶입니다. 포함된 이미지 제공 요청 접두사로 사용 `is`를 사용하는 포함된 이미지 렌더링 요청 `ir`, FXG 그래픽 렌더링 요청 `fxg`. 접두사가 지정되지 않은 경우 외부 서버 요청이 가정됩니다.

다음을 참조하십시오 [중첩 및 포함 요청](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b).

## 속성 {#section-2c22bb89a35d470f833df8ba898efd93}

레이어 속성입니다. 적용 대상 `layer=0` if `layer=comp`. 와 상호 배타적 `text=` 및 `textPs=` 동일한 레이어에서 다음 중 하나의 마지막 발생 `text=`, `textPs=`, 또는 `src=` 이 레이어를 우선하여 이미지 레이어인지 텍스트 레이어인지를 결정합니다. 효과 레이어에서 무시됨.

*`object`*다음을 포함하는 다른 카탈로그 레코드로 확인되지 않을 수 있음: `src=` 또는 `mask=` 명령 `catalog::Modifier`. (요청 중첩을 사용하여 유사한 효과를 얻을 수 있습니다.)

다음 `is`, `ir`, 및 `fxg` 접두사는 대/소문자를 구분합니다.

## 기본값 {#section-a92f3882041b4d43ae2caf014647165f}

레이어 0의 경우 다음과 같은 경우 URL의 경로 구성 요소에 있는 개체가 사용됩니다. `src=` 이(가) 지정되지 않았습니다. 다른 레이어의 기본값은 없습니다.

## 참조 {#section-e467e03330564796932ac081f1c9c1d0}

[catalog::Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) , [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494), [text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f), [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767), [마스크=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [오브젝트](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0), [템플릿](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [중첩 및 포함 요청](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
