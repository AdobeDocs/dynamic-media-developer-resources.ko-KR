---
description: FavoritesView.fmt
solution: Experience Manager
title: FavoritesView.fmt
uuid: 777411ee-c73f-4921-8ee1-7eb002ac3e95
feature: Dynamic Media Classic,뷰어,SDK/API,eCatalog 검색
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 4%

---


# FavoritesView.fmt{#favoritesview-fmt}

[!DNL `[FavoritesView.|<containerId>_favoritesView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`]

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> 이미지 서버에서 이미지를 로드하는 데 구성 요소에서 사용하는 이미지 형식을 지정합니다. 형식은 이미지 서버 및 클라이언트 브라우저에서 지원하는 모든 값입니다. </p> <p>이미지 형식이 <span class="codeph"> -alpha</span>로 끝나는 경우 구성 요소는 이미지를 투명한 컨텐츠로 렌더링합니다. 다른 모든 이미지 형식 값에 대해 구성 요소는 이미지를 불투명한 것으로 처리합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-f42369774e2740dcb399626a0e4e930e}

선택 사항입니다.

## 기본값 {#section-d016470e92a74f98a18c4ab3489410a5}

`jpeg`

## 예 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`fmt=png-alpha`
