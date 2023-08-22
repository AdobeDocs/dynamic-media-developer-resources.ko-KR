---
title: op_colorize
description: 이미지를 색상화합니다. 어두운 영역과 밝은 영역을 유지하면서 이미지 데이터를 색상화합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1abbde32-867a-4596-a46b-12ec50d59170
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '308'
ht-degree: 4%

---

# op_colorize{#op-colorize}

이미지를 색상화합니다. 어두운 영역과 밝은 영역을 유지하면서 이미지 데이터를 색상화합니다.

` op_colorize= *`색상`*[,off|norm[, *`대비`*]]`

<table id="simpletable_768D6CDF3F734E7F89DC7AB2EAAC0C77"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> color </span> </p> </td> 
  <td class="stentry"> <p>대체 RGB 색상. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 꺼짐 </span> </p> </td> 
  <td class="stentry"> <p>자동 밝기 보상을 비활성화합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 규범 </span> </p> </td> 
  <td class="stentry"> <p>자동 밝기 보상을 활성화합니다(기본값). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 대비 </span> </p> </td> 
  <td class="stentry"> <p>대비 범위(실수 0..100). 입력 대비를 유지하려면 0으로 설정합니다. </p> </td> 
 </tr> 
</table>

두 번째 인수는 색상화하기 전에 소스 이미지의 밝기를 조정해야 하는지 여부를 지정합니다. 지정 `off` 자동 밝기 보상을 비활성화하려면 `norm` 중간 값이 50% 세기가 되도록 밝기를 자동으로 조정합니다.

설정 *`contrast`* 값을 0으로 설정하여 입력 이미지의 대비 범위를 유지하거나 0보다 큰 값으로 원하는 대비 범위를 지정합니다. 값이 100이면 대비가 최대화됩니다. 일반적인 값은 30에서 70 사이일 수 있습니다.

기본 제공 밝기 및 대비 조정 외에도 `op_brightness=` 및 `op_contrast=` 색상화 효과를 더욱 세밀하게 조정하는 데 사용할 수 있습니다.

>[!NOTE]
>
>착색 알고리즘은 영상 데이터에서 휘도의 정보만을 사용한다. 이러한 회색 음영으로의 변환은 간단하며 색상 관리가 아닙니다. `op_colorize` 입력이 회색 음영 또는 CMYK인 경우에도 항상 RGB 데이터를 출력합니다.

## 속성 {#section-c0f8bd424b864153a1108f384939f55b}

레이어 명령. 다음과 같은 경우 현재 레이어 또는 합성 이미지에 적용됩니다. `layer=comp`. 효과 레이어에서 무시됨.

*`color`* 은(는) RGB 값이어야 합니다. 회색 또는 CMYK *`color`* 값은 지원되지 않습니다.

다음 *`contrast`* 밝기 보상이 꺼져 있으면 값이 무시됩니다.

*`color`* 의 픽셀 유형에 해당하는 작업 색상 공간에 존재한다고 가정합니다. *`color`*. *`color`* 병합 시 레이어 이미지의 픽셀 유형이 다른 경우 정확하게 변환됩니다.

CMYK 이미지는 작업을 적용하기 전에 RGB으로 변환됩니다.

## 기본값 {#section-0c3ea13efbac432c8970862d223e39b3}

`None`을 참조하십시오. 두 번째 및 세 번째 인수는 기본적으로 로 설정됩니다. `norm,0`: 자동 밝기 보상 및 대비 변경 없음

## 예 {#section-4c418d7b5e97409d9a448b8f08a1eab3}

이미지 레이어를 색상화하기 전에 밝기 및 대비를 동적으로 조정합니다.

… `&op_brightness=-15&op_contrast=22&op_colorize=a0b0c0&`…

대신 자동 밝기 및 대비 조정을 사용하십시오.

… `&op_colorize=a0b0c0,norm,50&`…

## 참조 {#section-5581eb0e03014fa795e8f078c60e6c8d}

[색상](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md), [op_brightness=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-brightness.md#reference-edf79dc41ae5411c80bec3ee3731c58a), [op_contrast=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-contrast.md#reference-b26dfa9869fd43bebea0fbb8e9fe743d), [색상 관리](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
