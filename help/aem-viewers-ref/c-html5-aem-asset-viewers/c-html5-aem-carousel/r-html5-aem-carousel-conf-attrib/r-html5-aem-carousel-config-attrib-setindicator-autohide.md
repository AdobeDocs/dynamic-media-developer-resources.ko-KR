---
title: SetIndicator.autohide
description: SetIndicator.autohide
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 75521239-a0be-4aa0-b65d-9a1f7d902cf2
TQID: 'https://experienceleague.adobe.com/3L6Dr9wnZCV-YCNkZ-kLmF-xZMn-sv1qCo7QeGT-CHU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 89
ht-degree: 3%

---

# SetIndicator.autohide{#setindicator-autohide}

` [SetIndicator.|<containerId>_setIndicator.]autohide=0|1[, *`제한`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">0|1[,<span class="varname"> 제한</span>]</span> </p> </td> 
   <td colname="col2"> <p> 페이지 수와 런타임 구성 요소 크기에 따라 자동 숨기기 행동을 구성합니다. </p> <p> <span class="codeph"> 0</span>이(가) 자동 숨기기를 끕니다. </p> <p> <span class="codeph"> 1</span>에서 자동 숨기기를 사용할 수 있습니다. 다음 조건 중 하나 이상이 참인 경우 구성 요소는 점을 숨깁니다. </p> <p> 
     <ul id="ul_A7F9C1DDC6AE44BAA348B3AD440A4EDD"> 
      <li id="li_39332158806445DF874C5A52F1331B8B">점이 있는 행이 런타임 구성 요소 너비보다 넓어지거나 </li> 
      <li id="li_E30BAC8B609147ADB8824000F5729B21">이 구성 요소에 대해 설정된 페이지 수가 <span class="codeph"><span class="varname"> limit</span></span> 매개 변수에 의해 구성된 한도를 초과합니다. </li> 
     </ul> </p> <p> <span class="codeph"><span class="varname"> limit</span></span>을(를) <span class="codeph"> -1</span>(으)로 설정하면 두 번째 자동 숨기기 조건이 비활성화됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택적.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

`1,10`

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`autohide=0`
