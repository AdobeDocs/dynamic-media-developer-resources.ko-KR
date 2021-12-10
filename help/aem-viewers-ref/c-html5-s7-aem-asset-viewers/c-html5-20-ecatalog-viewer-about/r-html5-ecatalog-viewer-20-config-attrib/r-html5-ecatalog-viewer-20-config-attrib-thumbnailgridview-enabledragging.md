---
title: ThumbnailGridView.enabledragging
description: ThumbnailGridView.enabledragging
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: e3615e82-d8f0-427e-ab32-f7d0f2b6cbf3
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 6%

---

# ThumbnailGridView.enabledragging{#thumbnailgridview-enabledragging}

` [ThumbnailGridView.|<containerId>_gridView.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_B1363BFD20204093AAB326A1AB503B93"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td> <p> 마우스로 또는 터치 제스처를 사용하여 견본을 스크롤하는 기능을 활성화하거나 비활성화합니다 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> <span class="varname"> overdragvalue </span> </span> </p> </td> 
   <td> <p> 함수 내의 <span class="codeph"> 0-1 </span> 범위. 이것은 <span class="codeph"> % </span> 실제 속도의 잘못된 방향으로의 이동에 대한 값. 로 설정된 경우 <span class="codeph"> 1 </span>마우스로 움직입니다. 로 설정된 경우 <span class="codeph"> 0 </span>그러나 잘못된 방향으로 전혀 움직이지 못하게 합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-831c23dea82449bfa50fd155bea365b7}

선택 사항입니다.

## 기본값 {#section-464be2db89f34516ad93f32f7783d2b0}

`1,0.5`

## 예 {#section-e67c8807762e471bb03d6a8fb20e19d4}

`enabledragging=0`
