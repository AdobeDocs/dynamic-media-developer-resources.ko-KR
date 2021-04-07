---
description: SetIndicator.autohide
solution: Experience Manager
title: SetIndicator.autohide
feature: Dynamic Media Classic,뷰어,SDK/API,회전판 배너
role: 개발자,비즈니스 전문가
exl-id: 75521239-a0be-4aa0-b65d-9a1f7d902cf2
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 5%

---

# SetIndicator.autohide{#setindicator-autohide}

` [SetIndicator.|<containerId>_setIndicator.]autohide=0|1[, *`제한`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">0|1[,<span class="varname"> 제한</span>]</span> </p> </td> 
   <td colname="col2"> <p> 페이지 수 및 런타임 구성 요소 크기에 따라 자동 숨기기 동작을 구성합니다. </p> <p> <span class="codeph"> 0</span> 은 자동 숨기기를 끕니다. </p> <p> <span class="codeph"> 1</span> 는 자동 숨기기를 활성화합니다. 다음 조건 중 하나 이상이 true로 전환되면 구성 요소는 해당 점을 숨깁니다. </p> <p> 
     <ul id="ul_A7F9C1DDC6AE44BAA348B3AD440A4EDD"> 
      <li id="li_39332158806445DF874C5A52F1331B8B">점이 있는 행은 런타임 구성 요소 폭보다 폭이 넓어지거나, </li> 
      <li id="li_E30BAC8B609147ADB8824000F5729B21">이 구성 요소에 대해 설정된 페이지 수가 <span class="codeph"><span class="varname"> 제한</span></span> 매개 변수로 구성된 제한을 초과합니다. </li> 
     </ul> </p> <p> <span class="codeph"><span class="varname"> limit</span></span>을 <span class="codeph"> -1</span>으로 설정하면 두 번째 자동 숨기기 조건이 비활성화됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택 사항입니다.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

`1,10`

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`autohide=0`
