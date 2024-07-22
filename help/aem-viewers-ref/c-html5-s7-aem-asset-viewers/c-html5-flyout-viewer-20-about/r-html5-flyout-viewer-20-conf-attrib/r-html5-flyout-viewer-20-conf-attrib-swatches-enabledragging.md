---
title: Swatches.enabledragging
description: Swatches.enabledragging
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 7ffdc886-5631-429f-84b4-4b32b715713d
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
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

## 속성 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

선택적.

## 기본값 {#section-a08032f0fcf041c09e63c0238a339fc9}

`1,0.5`

## 예 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`enabledragging=0`
