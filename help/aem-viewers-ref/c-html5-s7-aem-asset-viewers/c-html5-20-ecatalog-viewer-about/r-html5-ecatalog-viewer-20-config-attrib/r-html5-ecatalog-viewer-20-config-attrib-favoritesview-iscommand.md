---
title: FavoritesView.iscommand
description: 모든 축소판에 적용되는 이미지 제공 명령 문자열입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 1b6198f4-367d-437a-b8b1-206519567af0
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 8%

---

# FavoritesView.iscommand{#favoritesview-iscommand}

모든 축소판에 적용되는 이미지 제공 명령 문자열입니다.

` [FavoritesView.|<containerId>_favoritesView.]iscommand= *`isCommand`*`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> URL에 지정된 경우 다음과 같은 모든 항목이 <span class="codeph"> &amp;</span> 및 <span class="codeph"> =</span> 는 HTTP로 인코딩되어야 합니다. <span class="codeph"> %26</span> 및 <span class="codeph"> %3D</span>각각 입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-f42369774e2740dcb399626a0e4e930e}

선택 사항입니다.

## 기본값 {#section-d016470e92a74f98a18c4ab3489410a5}

없음.

## 예 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

뷰어 URL에 지정된 경우.

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

구성 데이터에 지정되는 경우.

`iscommand=op_sharpen=1&op_colorize=0xff0000`
