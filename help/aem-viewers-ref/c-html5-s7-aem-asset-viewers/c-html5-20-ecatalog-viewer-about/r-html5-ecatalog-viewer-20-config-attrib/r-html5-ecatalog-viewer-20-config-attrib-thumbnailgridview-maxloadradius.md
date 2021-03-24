---
description: ThumbnailGridView.maxloadradius
solution: Experience Manager
title: ThumbnailGridView.maxloadradius
feature: Dynamic Media Classic,뷰어,SDK/API,eCatalog
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 6%

---


# ThumbnailGridView.maxloadradius{#thumbnailgridview-maxloadradius}

` [ThumbnailGridView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_D29F1F6A8EC74F42A254C823435F9493"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>구성 요소 미리 로드 동작을 지정합니다. </p> <p><span class="codeph"> -1</span>으로 설정하면 구성 요소가 초기화되거나 에셋이 변경될 때 축소판이 동시에 로드됩니다. </p> <p><span class="codeph"> 0</span>으로 설정하면 보이는 축소판만 로드됩니다. </p> <p><span class="codeph"><span class="varname"> preloadnbr</span></span> 설정은 표시 영역 주위에 미리 로드되는 보이지 않는 행/열의 수를 정의합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-a3abd04c03e14c238a07349ce50d8310}

선택 사항입니다.

## 기본값 {#section-c60e81667965460cbf03378a1ab9b187}

`1`

## 예 {#section-472614b59e04430490a7f16c932bce89}

`maxloadradius=0`
