---
description: Swatches.enabledragging
solution: Experience Manager
title: Swatches.enabledragging
uuid: fbff46d7-f947-40ae-9a0c-7d2496a343f6
feature: Dynamic Media Classic,뷰어,SDK/API,인라인 확대/축소
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 5%

---


# Swatches.enabledragging{#swatches-enabledragging}

` [Swatches.|<containerId>_swatches.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_B1363BFD20204093AAB326A1AB503B93"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td> <p> 사용자가 마우스로 견본을 스크롤하거나 터치 제스처를 사용하여 견본을 스크롤할 수 있는 기능을 활성화하거나 비활성화합니다 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> <span class="varname"> overdragvalue  </span> </span> </p> </td> 
   <td> <p> <span class="codeph"> 0-1 </span> 범위 내의 함수입니다. 실제 속도의 잘못된 방향으로 이동하는 경우 <span class="codeph"> % </span> 값입니다. <span class="codeph"> 1 </span>으로 설정하면 마우스와 함께 이동합니다. <span class="codeph"> 0 </span>으로 설정된 경우 잘못된 방향으로 이동할 수 없습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-e6310c8c4e8547689a5b48ceddb3671d}

선택 사항입니다.

## 기본값 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`1,0.5`

## 예 {#section-3a188ab955c445bcb2efa3c49722c10d}

`enabledragging=0`
