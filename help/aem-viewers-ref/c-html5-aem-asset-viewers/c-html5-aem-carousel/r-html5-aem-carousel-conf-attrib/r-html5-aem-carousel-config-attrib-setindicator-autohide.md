---
description: 널
seo-description: 널
seo-title: SetIndicator.autohide
solution: Experience Manager
title: SetIndicator.autohide
topic: Dynamic media
uuid: eb93ad7a-6176-47ed-92c6-2eb1afcac0eb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SetIndicator.autohide{#setindicator-autohide}

` [SetIndicator.|<containerId>_setIndicator.]autohide=0|1[, *`제한`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">0|1[,<span class="varname"> 제한</span>]</span> </p> </td> 
   <td colname="col2"> <p> 페이지 수 및 런타임 구성 요소 크기에 따라 자동 숨기기 동작을 구성합니다. </p> <p> <span class="codeph"> 0을</span> 사용하면 자동 숨기기가 꺼집니다. </p> <p> <span class="codeph"> 1</span> 자동 숨기기를 활성화합니다. 다음 조건 중 하나 이상이 true로 전환되면 구성 요소는 해당 점을 숨깁니다. </p> <p> 
     <ul id="ul_A7F9C1DDC6AE44BAA348B3AD440A4EDD"> 
      <li id="li_39332158806445DF874C5A52F1331B8B">점이 있는 행은 런타임 구성 요소 너비보다 넓어집니다. </li> 
      <li id="li_E30BAC8B609147ADB8824000F5729B21">이 구성 요소에 대해 설정된 페이지 수가 <span class="codeph"><span class="varname"> 제한</span></span> 매개 변수에 의해 구성된 제한을 초과합니다. </li> 
     </ul> </p> <p> 제한을 <span class="codeph"><span class="varname"></span></span> -1 <span class="codeph"></span> (으)로 설정하면 두 번째 자동 숨기기 조건이 비활성화됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택 사항입니다.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

`1,10`

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`autohide=0`
