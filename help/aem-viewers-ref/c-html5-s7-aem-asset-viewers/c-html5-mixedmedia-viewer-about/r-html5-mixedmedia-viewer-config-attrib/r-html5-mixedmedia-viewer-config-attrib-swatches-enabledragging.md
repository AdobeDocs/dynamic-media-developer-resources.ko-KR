---
description: Swatches.enabledragging
solution: Experience Manager
title: Swatches.enabledragging
feature: Dynamic Media Classic,Viewers,SDK/API,혼합 미디어 집합
role: Developer,Business Practitioner
exl-id: fd432573-677f-4c46-9cc1-88089496ce75
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 5%

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

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택 사항입니다.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,0.5`

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`enabledragging=0`
