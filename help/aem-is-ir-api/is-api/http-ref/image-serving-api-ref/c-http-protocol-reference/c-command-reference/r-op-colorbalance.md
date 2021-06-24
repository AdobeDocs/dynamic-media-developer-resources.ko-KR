---
description: 색상 균형을 조정합니다. 각 RGB 색상 구성 요소의 값을 개별적으로 조정합니다.
solution: Experience Manager
title: op_colorbalance
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 93476778-97b0-4ad5-b22a-093239e845f0
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 2%

---

# op_colorbalance{#op-colorbalance}

색상 균형을 조정합니다. 각 RGB 색상 구성 요소의 값을 개별적으로 조정합니다.

`op_colorbalance= *``*, *``*, *`redAdjustgreenAdj`*`

<table id="simpletable_BBDAA6FE9A0E48E3BD8304BDED776713"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> redAdj</span> </p></td> 
  <td class="stentry"> <p>빨간색 구성 요소 조정(-100...+100 int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> greenAdj</span> </p></td> 
  <td class="stentry"> <p>녹색 구성 요소 조정(-100..+100 int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> blueAdj</span> </p></td> 
  <td class="stentry"> <p>파란색 구성 요소 조정(-100..+100 int). </p></td> 
 </tr> 
</table>

색상 관리를 활성화하면 정확하지 않은 기본 변환을 사용하여 회색 및 CMYK 입력 이미지 데이터가 RGB로 변환됩니다.

## 속성 {#section-dff9c934f7c1442bbd02379b688d82e2}

레이어 명령. `layer=comp` 인 경우 현재 레이어 또는 복합 이미지에 적용됩니다. 효과 레이어에서 무시됨. 작업이 적용되기 전에 CMYK 이미지 및 레이어가 RGB로 변환됩니다.

## 기본값 {#section-08d84ef715964f7daea86f5ef237d199}

`op_colorbalance=0,0,0` 색상은 변경되지 않습니다.

## 예 {#section-7e97fa36e01d4af8ab03fc9d493da1a1}

색상 균형을 빨간색으로 푸시합니다.

… `&op_colorBalance=100,0,0&`…
