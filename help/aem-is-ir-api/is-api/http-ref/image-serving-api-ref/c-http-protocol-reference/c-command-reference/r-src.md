---
description: 레이어 이미지.
seo-description: 레이어 이미지.
seo-title: src
solution: Experience Manager
title: src
uuid: b4396848-b992-4371-a8ae-4ff1781ae1be
feature: Dynamic Media Classic,SDK/API
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 2%

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
  <td class="stentry"> <p>중첩된 이미지 제공, 이미지 렌더링 또는 외부 요청. </p> </td> 
 </tr> 
</table>

## 설명 {#section-59ec6dc2afcb43efb34dbb0f7733543f}

이미지 레이어의 소스 이미지를 지정합니다.

*`object`* 카탈로그 항목 또는 이미지/SVG 파일일 수 있습니다.

[object](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)을 참조하십시오.

중첩 또는 포함된 요청은 중괄호로 묶입니다. 포함된 이미지 제공 요청에 `is`, `ir`로 포함된 이미지 렌더링 요청 및 `fxg`로 FXG 그래픽 렌더링 요청을 접두어로 지정합니다. 접두어가 지정되지 않은 경우 외국 서버에 대한 요청은 가정합니다.

[요청 중첩 및 포함](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)을 참조하십시오.

## 속성 {#section-2c22bb89a35d470f833df8ba898efd93}

레이어 속성입니다. `layer=comp`인 경우 `layer=0`에 적용됩니다. 동일한 레이어의 `text=` 및 `textPs=`과 함께 사용할 수 없습니다.`text=`, `textPs=` 또는 `src=`의 마지막 항목이 실행되어 이미지나 텍스트 레이어인지 확인합니다. 효과 레이어에서 무시됩니다.

*`object`*은 `catalog::Modifier`에 `src=` 또는 `mask=` 명령을 포함하는 다른 카탈로그 레코드로 확인할 수 없습니다. 요청 중첩을 사용하여 비슷한 효과를 낼 수 있습니다.

`is`, `ir` 및 `fxg` 접두사는 대/소문자를 구분합니다.

## 기본값 {#section-a92f3882041b4d43ae2caf014647165f}

레이어 0의 경우 `src=`이(가) 지정되지 않은 경우 URL의 경로 구성 요소의 객체가 사용됩니다. 다른 레이어의 기본값은 없습니다.

## 참조 {#section-e467e03330564796932ac081f1c9c1d0}

[카탈로그::Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) ,  [속성::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494),  [text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f),  [textPs텍스트](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)  [, mask=, object, object, 템플릿템플릿, 중첩 및 포함 요청 포함](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
