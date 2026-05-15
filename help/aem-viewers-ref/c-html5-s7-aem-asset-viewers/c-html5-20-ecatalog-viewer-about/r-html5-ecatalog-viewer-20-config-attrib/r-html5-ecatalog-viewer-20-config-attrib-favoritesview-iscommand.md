---
title: FavoritesView.iscommand
description: 모든 썸네일에 적용되는 이미지 제공 명령 문자열.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 1b6198f4-367d-437a-b8b1-206519567af0
TQID: 'https://experienceleague.adobe.com/07R-e5T13wkEDybF0r96CG3DRfGWq6sxTIVVhgZ-HA8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 61
ht-degree: 6%

---

# FavoritesView.iscommand{#favoritesview-iscommand}

모든 썸네일에 적용되는 이미지 제공 명령 문자열.

` [FavoritesView.|<containerId>_favoritesView.]iscommand= *`isCommand`*`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> URL에 지정되는 경우 <span class="codeph"> &amp;</span> 및 <span class="codeph"> =</span>은(는) 각각 <span class="codeph"> %26</span> 및 <span class="codeph"> %3D</span>(으)로 HTTP 인코딩이 적용되어야 합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-f42369774e2740dcb399626a0e4e930e}

선택적.

## 기본값 {#section-d016470e92a74f98a18c4ab3489410a5}

없음.

## 예 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

뷰어 URL에 지정되는 경우.

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

구성 데이터에 지정된 경우.

`iscommand=op_sharpen=1&op_colorize=0xff0000`
