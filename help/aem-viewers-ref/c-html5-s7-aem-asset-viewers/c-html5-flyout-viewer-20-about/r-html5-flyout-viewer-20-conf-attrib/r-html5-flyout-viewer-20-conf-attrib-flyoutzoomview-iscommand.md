---
description: FlyoutZoomView.iscommand
solution: Experience Manager
title: FlyoutZoomView.iscommand
feature: Dynamic Media Classic,Viewers,SDK/API,플라이아웃
role: Developer,User
exl-id: b23918b5-5fc6-4038-b6f5-519198a96f86
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 6%

---

# FlyoutZoomView.iscommand{#flyoutzoomview-iscommand}

` [FlyoutZoomView.|<containerId>_flyout.]iscommand= *`isCommand`*`

<table id="table_43A84C1044574A6FAB8CE67D71AAD5EC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isCommand</span> </span> </p> </td> 
   <td colname="col2"> <p> </p> <p>FlyoutZoomView 기본 이미지와 확대 보기에 적용되는 이미지 제공 명령 문자열입니다. URL에 지정된 경우 HTTP를 통해 <span class="codeph"> &amp;</span> 및 <span class="codeph"> =</span>의 모든 항목을 <span class="codeph"> %26</span> 및 <span class="codeph"> %3D</span>로 각각 인코딩해야 합니다. </p> <p> <p>참고:  이미지 크기 조정 조작 명령은 지원되지 않습니다. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

선택 사항입니다.

## 기본값 {#section-a08032f0fcf041c09e63c0238a339fc9}

없음.

## 예 {#section-0338be21edd04ff1a3bed5c8319b61a4}

뷰어 URL에 지정된 경우:

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

구성 데이터에 지정된 경우:

`iscommand=op_sharpen=1&op_colorize=0xff0000`
