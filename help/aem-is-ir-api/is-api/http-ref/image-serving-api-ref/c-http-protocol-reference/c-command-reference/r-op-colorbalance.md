---
title: op_colorbalance
description: 색상 균형을 조정합니다. 각 RGB 색상 구성 요소의 값을 개별적으로 조정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 93476778-97b0-4ad5-b22a-093239e845f0
TQID: 'https://experienceleague.adobe.com/etLnTD-hMe5kOnvak7n47O0XwOWvqtC5av4FkYZpaGI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 114
ht-degree: 1%

---

# op_colorbalance{#op-colorbalance}

색상 균형을 조정합니다. 각 RGB 색상 구성 요소의 값을 개별적으로 조정합니다.

`op_colorbalance= *`redAdj`*, *`greenAdj`*, *`blueAdj`*`

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

회색 및 CMYK 입력 이미지 데이터는 색상 관리가 활성화되어 있을 때 정확하지 않은 나이브 변환을 사용하여 RGB으로 변환됩니다.

## 속성 {#section-dff9c934f7c1442bbd02379b688d82e2}

레이어 명령. `layer=comp`인 경우 현재 레이어 또는 합성 이미지에 적용됩니다. 효과 레이어에서 무시됨. CMYK 이미지 및 레이어는 작업을 적용하기 전에 RGB으로 변환됩니다.

## 기본값 {#section-08d84ef715964f7daea86f5ef237d199}

`op_colorbalance=0,0,0`(색상 변경 없음).

## 예 {#section-7e97fa36e01d4af8ab03fc9d493da1a1}

색상 균형을 빨간색으로 푸시합니다.

... `&op_colorBalance=100,0,0&`..
