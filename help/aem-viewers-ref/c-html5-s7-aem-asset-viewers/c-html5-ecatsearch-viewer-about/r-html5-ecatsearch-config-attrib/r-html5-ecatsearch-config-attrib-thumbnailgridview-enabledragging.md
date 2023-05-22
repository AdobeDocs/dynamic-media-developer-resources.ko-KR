---
description: ThumbnailGridView.enabledragging
solution: Experience Manager
title: ThumbnailGridView.enabledragging
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 011ef772-6760-4794-819e-2a822fbae1b5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 5%

---

# ThumbnailGridView.enabledragging{#thumbnailgridview-enabledragging}

[!DNL `[ThumbnailGridView.|<containerId>_gridView.]enabledragging=0|1[, *`overdragvalue`*]`]

<table id="table_B1363BFD20204093AAB326A1AB503B93"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td> <p> 사용자가 마우스나 터치 제스처를 사용하여 견본을 스크롤하는 기능을 활성화하거나 비활성화합니다 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> <span class="varname"> overdragvalue </span> </span> </p> </td> 
   <td> <p> 내의 함수 <span class="codeph"> 0-1 </span> 범위. 다음입니다. <span class="codeph"> % </span> 실제 속도의 잘못된 방향 이동에 대한 값. 로 설정된 경우 <span class="codeph"> 1 </span>마우스와 함께 이동합니다. 로 설정된 경우 <span class="codeph"> 0 </span>즉, 잘못된 방향으로 전혀 이동할 수 없습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-831c23dea82449bfa50fd155bea365b7}

선택적.

## 기본값 {#section-464be2db89f34516ad93f32f7783d2b0}

[!DNL `1,0.5`]

## 예 {#section-e67c8807762e471bb03d6a8fb20e19d4}

[!DNL `enabledragging=0`]
