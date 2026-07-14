---
title: ThumbnailGridView.maxloadradius
description: ThumbnailGridView.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: e93de3b5-b42d-4db8-90b9-9e2aa53af775
TQID: 'https://experienceleague.adobe.com/dbcZzhrzwZU5T307jcD6H6kx5RNeYWRBe21nD-2deXU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f6432244ef9faba7a81488e9de8e438154ae6123
workflow-type: tm+mt
source-wordcount: 58
ht-degree: 5%

---

# ThumbnailGridView.maxloadradius{#thumbnailgridview-maxloadradius}

` [ThumbnailGridView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_D29F1F6A8EC74F42A254C823435F9493"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>구성 요소 미리 로드 동작을 지정합니다. </p> <p><span class="codeph"> -1</span>(으)로 설정된 경우 구성 요소가 초기화되거나 자산이 변경될 때 썸네일이 동시에 로드됩니다. </p> <p><span class="codeph"> 0</span>(으)로 설정하면 표시되는 축소판만 로드됩니다. </p> <p>Set <span class="codeph"><span class="varname"> preloadnbr</span></span>은(는) 표시되는 영역 주위에서 사전 로드되는 표시되지 않는 행/열의 수를 정의합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-a3abd04c03e14c238a07349ce50d8310}

선택적.

## 기본값 {#section-c60e81667965460cbf03378a1ab9b187}

`1`

## 예 {#section-472614b59e04430490a7f16c932bce89}

`maxloadradius=0`

