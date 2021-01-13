---
description: FavoritesView.maxloadradius
solution: Experience Manager
title: FavoritesView.maxloadradius
topic: Dynamic media
uuid: 52347bee-2cdf-4bb4-bb6f-eefff06b82af
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 7%

---


# FavoritesView.maxloadradius{#favoritesview-maxloadradius}

` [FavoritesView.|<containerId>_favoritesView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> 구성 요소 미리 로드 동작을 지정합니다. </p> <p><span class="codeph"> -1</span>으로 설정하면 구성 요소가 초기화되거나 자산이 변경될 때 모든 축소판이 동시에 로드됩니다. </p> <p><span class="codeph"> 0</span>으로 설정하면 보이는 축소판만 로드됩니다. </p> <p> <span class="codeph"><span class="varname"> preloadnbr</span></span>로 설정하면 표시 영역 주위에 미리 로드되는 보이지 않는 행 수를 지정할 수 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-f42369774e2740dcb399626a0e4e930e}

선택 사항입니다.

## 기본값 {#section-d016470e92a74f98a18c4ab3489410a5}

`1`

## 예 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`maxloadradius=0`
