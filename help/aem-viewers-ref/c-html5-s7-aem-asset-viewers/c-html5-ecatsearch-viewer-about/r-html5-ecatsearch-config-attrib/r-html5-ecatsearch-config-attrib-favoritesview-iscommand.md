---
description: 모든 축소판에 적용되는 이미지 제공 명령 문자열.
seo-description: 모든 축소판에 적용되는 이미지 제공 명령 문자열.
seo-title: FavoritesView.iscommand
solution: Experience Manager
title: FavoritesView.iscommand
topic: Dynamic media
uuid: be3d49d1-d5d2-4ecd-bc8f-fe5f80204c76
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 7%

---


# FavoritesView.iscommand{#favoritesview-iscommand}

모든 축소판에 적용되는 이미지 제공 명령 문자열.

[!DNL `[FavoritesView.|<containerId>_favoritesView.]iscommand= *`isCommand`*`]

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> URL에 지정된 경우 <span class="codeph"> &amp;</span> 및 <span class="codeph"> =</span>의 모든 항목은 각각 <span class="codeph"> %26</span> 및 <span class="codeph"> %3D</span>으로 HTTP로 인코딩되어야 합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-f42369774e2740dcb399626a0e4e930e}

선택 사항입니다.

## 기본값 {#section-d016470e92a74f98a18c4ab3489410a5}

없음.

## 예 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

뷰어 URL에 지정된 경우.

[!DNL `iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`]

구성 데이터에 지정된 경우입니다.

[!DNL `iscommand=op_sharpen=1&op_colorize=0xff0000`]
