---
title: Swatches.enabledragging
description: Swatches.enabledragging
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 6ae18f94-7a0f-429e-9684-eff43f523b1d
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 3%

---

# Swatches.enabledragging{#swatches-enabledragging}

` [Swatches.|<containerId>_swatches.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_B1363BFD20204093AAB326A1AB503B93"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td> <p> 사용자가 마우스나 터치 제스처를 사용하여 견본을 스크롤하는 기능을 활성화하거나 비활성화합니다 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> <span class="varname"> overdragvalue </span> </span> </p> </td> 
   <td> <p> <span class="codeph"> 0-1 </span> 범위 내의 함수입니다. 실제 속도의 잘못된 방향 이동에 대한 <span class="codeph"> % </span> 값입니다. <span class="codeph"> 1 </span>(으)로 설정된 경우 마우스와 함께 이동합니다. <span class="codeph"> 0 </span>(으)로 설정된 경우 잘못된 방향으로 전혀 이동할 수 없습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택적.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

`1,0.5`

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`enabledragging=0`
