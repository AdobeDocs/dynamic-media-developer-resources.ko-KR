---
description: 이미지 색상화 어두운 영역과 밝은 영역을 그대로 유지하면서 이미지 데이터에 색상을 적용합니다.
seo-description: 이미지 색상화 어두운 영역과 밝은 영역을 그대로 유지하면서 이미지 데이터에 색상을 적용합니다.
seo-title: op_coloriize
solution: Experience Manager
title: op_coloriize
topic: Scene7 Image Serving - Image Rendering API
uuid: e74a85ca-73bf-4c69-ac77-768a58b33d0b
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150

---


# op_coloriize{#op-colorize}

이미지 색상화 어두운 영역과 밝은 영역을 그대로 유지하면서 이미지 데이터에 색상을 적용합니다.

` op_colorize= *``*[,off|norm[, *`색상 대비`*]]`

<table id="simpletable_768D6CDF3F734E7F89DC7AB2EAAC0C77"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> color </span> </p> </td> 
  <td class="stentry"> <p>대체 RGB 색상. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 꺼짐 </span> </p> </td> 
  <td class="stentry"> <p>자동 명도 보정을 비활성화합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 규범 </span> </p> </td> 
  <td class="stentry"> <p>자동 밝기 보정(기본값)을 활성화합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 대비 </span> </p> </td> 
  <td class="stentry"> <p>대비 범위(실제 0.100);0으로 설정하면 입력 대비가 유지됩니다. </p> </td> 
 </tr> 
</table>

두 번째 인수는 색상을 지정하기 전에 소스 이미지의 밝기를 조정할지 여부를 지정합니다. 자동 명도 `off` `norm` 보정을 비활성화하거나 중간값 값이 50%가 되도록 밝기를 자동으로 조정하도록 지정합니다.

Set the *`contrast`* value to 0 to preserve the contrast range of the input image, or specify a desired contrast range with a value greater than 0. 값이 100이면 대비가 최대화됩니다. 일반적인 값은 30에서 70 사이일 수 있습니다.

내장된 밝기 및 대비 조정 외에도 색상을 세부적으로 조정하는 데 사용할 `op_brightness=` 수 `op_contrast=` 있습니다.

>[!NOTE]
>
>색상화 알고리즘은 이미지 데이터의 광도 정보만 사용합니다. 이 회색 음영으로 변환하는 작업은 간단하며 색상 관리가 아닙니다. `op_colorize` 입력이 회색 음영이나 CMYK인 경우에도 항상 RGB 데이터를 출력합니다.

## 속성 {#section-c0f8bd424b864153a1108f384939f55b}

레이어 명령. 현재 레이어 또는 합성 이미지에 적용됩니다( `layer=comp`경우). 효과 레이어에서 무시됩니다.

*`color`* 은(는) RGB 값이어야 합니다.회색 또는 CMYK *`color`* 값은 지원되지 않습니다.

밝기 보정이 꺼지면 *`contrast`* 값이 무시됩니다.

*`color`* 는 의 픽셀 유형에 해당하는 작업 색상 공간에 존재하는 것으로 *`color`*&#x200B;가정합니다. *`color`* 는 레이어 이미지에 병합 시 다른 픽셀 유형이 있는 경우 정확하게 변환됩니다.

CMYK 이미지는 작업이 적용되기 전에 RGB로 변환됩니다.

## 기본값 {#section-0c3ea13efbac432c8970862d223e39b3}

`None`에 대한 값 중 하나를 선택합니다. 두 번째 및 세 번째 인수는 `norm,0`자동 명도 보정을 위해 기본적으로 사용되며 대비는 변경되지 않습니다.

## 예 {#section-4c418d7b5e97409d9a448b8f08a1eab3}

이미지 레이어를 색상화하기 전에 명도 및 대비를 동적으로 조정합니다.

… `&op_brightness=-15&op_contrast=22&op_colorize=a0b0c0&`…

대신 자동 밝기 및 대비 조정 사용:

… `&op_colorize=a0b0c0,norm,50&`…

## 참조 {#section-5581eb0e03014fa795e8f078c60e6c8d}

[color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md), [op_brightness=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-brightness.md#reference-edf79dc41ae5411c80bec3ee3731c58a), [op_contrast=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-contrast.md#reference-b26dfa9869fd43bebea0fbb8e9fe743d), [색상 관리](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
