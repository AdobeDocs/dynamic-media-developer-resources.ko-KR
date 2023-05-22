---
description: 모든 썸네일에 적용되는 이미지 제공 명령 문자열.
solution: Experience Manager
title: FavoritesView.iscommand
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 114cc5b7-32b9-4d16-ab93-a66f3ec666e0
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 6%

---

# FavoritesView.iscommand{#favoritesview-iscommand}

모든 썸네일에 적용되는 이미지 제공 명령 문자열.

[!DNL `[FavoritesView.|<containerId>_favoritesView.]iscommand= *`isCommand`*`]

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> URL에 지정되는 경우 <span class="codeph"> 및</span> 및 <span class="codeph"> =</span> 은(는) (으)로 HTTP 인코딩되어야 합니다. <span class="codeph"> %26</span> 및 <span class="codeph"> %3D</span>, 각각 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-f42369774e2740dcb399626a0e4e930e}

선택적.

## 기본값 {#section-d016470e92a74f98a18c4ab3489410a5}

없음.

## 예 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

뷰어 URL에 지정되는 경우.

[!DNL `iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`]

구성 데이터에 지정된 경우.

[!DNL `iscommand=op_sharpen=1&op_colorize=0xff0000`]
