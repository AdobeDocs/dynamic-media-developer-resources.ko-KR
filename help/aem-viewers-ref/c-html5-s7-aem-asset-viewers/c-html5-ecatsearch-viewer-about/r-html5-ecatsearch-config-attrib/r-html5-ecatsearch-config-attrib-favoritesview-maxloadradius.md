---
description: FavoritesView.maxloadradius
solution: Experience Manager
title: FavoritesView.maxloadradius
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 440f147e-865c-4615-8d83-ea6431271612
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 5%

---

# FavoritesView.maxloadradius{#favoritesview-maxloadradius}

[!DNL `[FavoritesView.|<containerId>_favoritesView.]maxloadradius=-1|0| *`preloadnbr`*`]

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> 구성 요소 미리 로드 동작을 지정합니다. </p> <p>로 설정된 경우 <span class="codeph"> -1</span>, 구성 요소가 초기화되거나 자산이 변경될 때 모든 썸네일이 동시에 로드됩니다. </p> <p>로 설정된 경우 <span class="codeph"> 0</span>, 표시되는 축소판만 로드됩니다. </p> <p> 로 설정된 경우 <span class="codeph"><span class="varname"> preloadnbr</span></span>, 표시되는 영역 주위에서 사전 로드되는 표시되지 않는 행 수를 지정할 수 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-f42369774e2740dcb399626a0e4e930e}

선택적.

## 기본값 {#section-d016470e92a74f98a18c4ab3489410a5}

[!DNL `1`]

## 예 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

[!DNL `maxloadradius=0`]
