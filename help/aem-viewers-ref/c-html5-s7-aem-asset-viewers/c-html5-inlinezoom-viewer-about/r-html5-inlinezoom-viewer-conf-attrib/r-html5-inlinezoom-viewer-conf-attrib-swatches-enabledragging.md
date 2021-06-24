---
description: Swatches.enabledragging
solution: Experience Manager
title: Swatches.enabledragging
feature: Dynamic Media Classic,Viewers,SDK/API,인라인 확대/축소
role: Developer,Business Practitioner
exl-id: 9b69f6d7-b7a1-42c6-98d7-80952b7f8b31
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 6%

---

# Swatches.enabledragging{#swatches-enabledragging}

` [Swatches.|<containerId>_swatches.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_B1363BFD20204093AAB326A1AB503B93"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td> <p> 마우스로 또는 터치 제스처를 사용하여 견본을 스크롤하는 기능을 활성화하거나 비활성화합니다 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> <span class="varname"> overdragvalue  </span> </span> </p> </td> 
   <td> <p> <span class="codeph"> 0-1 </span> 범위 내의 함수입니다. 실제 속도의 잘못된 방향으로 이동하기 위한 <span class="codeph">% </span> 값입니다. <span class="codeph"> 1 </span>로 설정하면 마우스로 이동합니다. <span class="codeph"> 0 </span> 로 설정되어 있으면 전혀 잘못된 방향으로 이동할 수 없습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-e6310c8c4e8547689a5b48ceddb3671d}

선택 사항입니다.

## 기본값 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`1,0.5`

## 예 {#section-3a188ab955c445bcb2efa3c49722c10d}

`enabledragging=0`
