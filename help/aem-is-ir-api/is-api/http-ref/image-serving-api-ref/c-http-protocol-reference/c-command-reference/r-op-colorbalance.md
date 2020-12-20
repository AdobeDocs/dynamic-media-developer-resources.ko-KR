---
description: 색상 균형을 조정합니다. 각 RGB 색상 구성 요소의 값을 별도로 조정합니다.
seo-description: 색상 균형을 조정합니다. 각 RGB 색상 구성 요소의 값을 별도로 조정합니다.
seo-title: op_colorbalance
solution: Experience Manager
title: op_colorbalance
topic: Scene7 Image Serving - Image Rendering API
uuid: 177aa6e3-1b32-4254-85f1-d7fe14116e3c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 2%

---


# op_colorbalance{#op-colorbalance}

색상 균형을 조정합니다. 각 RGB 색상 구성 요소의 값을 별도로 조정합니다.

`op_colorbalance= *``*, *``*, *`redAdjugreenAdj`*`

<table id="simpletable_BBDAA6FE9A0E48E3BD8304BDED776713"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> redAdj</span> </p></td> 
  <td class="stentry"> <p>빨간색 구성 요소 조정(-100...+100 int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> greenAdj</span> </p></td> 
  <td class="stentry"> <p>녹색 구성 요소 조정(-100...+100 int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> blueAdj</span> </p></td> 
  <td class="stentry"> <p>파란색 구성 요소 조정(-100...+100 int). </p></td> 
 </tr> 
</table>

색상 관리를 사용하는 경우 정확하지 않은 기본 변환을 사용하여 회색 및 CMYK 입력 이미지 데이터가 RGB로 변환됩니다.

## 속성 {#section-dff9c934f7c1442bbd02379b688d82e2}

레이어 명령. `layer=comp`인 경우 현재 레이어나 합성 이미지에 적용됩니다. 효과 레이어에서 무시됩니다. CMYK 이미지 및 레이어는 작업이 적용되기 전에 RGB로 변환됩니다.

## 기본값 {#section-08d84ef715964f7daea86f5ef237d199}

`op_colorbalance=0,0,0` 색상을 변경하지 마십시오.

## 예 {#section-7e97fa36e01d4af8ab03fc9d493da1a1}

색상 균형을 빨간색으로 밀기:

… `&op_colorBalance=100,0,0&`…
