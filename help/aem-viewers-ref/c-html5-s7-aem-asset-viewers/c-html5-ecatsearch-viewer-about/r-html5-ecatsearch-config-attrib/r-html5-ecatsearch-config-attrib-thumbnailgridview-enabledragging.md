---
description: ThumbnailGridView.enabledragging
solution: Experience Manager
title: ThumbnailGridView.enabledragging
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 011ef772-6760-4794-819e-2a822fbae1b5
TQID: 'https://experienceleague.adobe.com/R-8C-obmM18dPSWcLrekSvAzSRRTrthSDePpybEcCOc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 939895a2a379b02e733e48932434433bfa9663e1
workflow-type: tm+mt
source-wordcount: 80
ht-degree: 6%

---

# ThumbnailGridView.enabledragging{#thumbnailgridview-enabledragging}

[!DNL `[ThumbnailGridView.|<containerId>_gridView.]enabledragging=0|1[, *`overdragvalue`*]`]

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

## 속성 {#section-831c23dea82449bfa50fd155bea365b7}

선택적.

## 기본값 {#section-464be2db89f34516ad93f32f7783d2b0}

[!DNL `1,0.5`]

## 예 {#section-e67c8807762e471bb03d6a8fb20e19d4}

[!DNL `enabledragging=0`]
