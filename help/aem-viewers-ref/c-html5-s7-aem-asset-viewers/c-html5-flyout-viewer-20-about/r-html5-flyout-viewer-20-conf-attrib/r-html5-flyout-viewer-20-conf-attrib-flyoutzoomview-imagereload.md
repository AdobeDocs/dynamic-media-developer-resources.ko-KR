---
description: FlyoutZoomView.imagereload
solution: Experience Manager
title: FlyoutZoomView.imagereload
feature: Dynamic Media Classic,Viewers,SDK/API,플라이아웃
role: Developer,User
exl-id: 483fa64b-5196-4477-8ea6-0f32c6557f72
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 4%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *``*[; *`너비`*]]`

<table id="table_42CA0074AD7C4F0D9FC81E9FCB0591C0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 크기 조정 중에 구성 요소가 기본 및 플라이아웃 보기에 대한 새 이미지를 가져오는 방법을 구성합니다. </p> <p><span class="codeph"> 0 </span> 로 설정하면 구성 요소가 크기 조정 중에 새 이미지를 로드하지 않습니다. 플라이아웃 보기의 이미지 해상도는 변경되지 않습니다. </p> <p><span class="codeph"> 1 </span>로 설정하면 기본 보기에 로드되는 이미지에 대해 하나 이상의 너비 중단점을 지정할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 중단점,  <span class="varname"> 너비  </span>[;  <span class="varname"> 너비  </span>]  </span> </p> </td> 
   <td colname="col2"> <p> 기본 보기에 로드되는 이미지의 너비 중단점. 구성 요소는 항상 초기 로드에 가장 적합한 크기를 사용합니다. 크기를 조정하면 기본 보기의 이미지가 항상 가장 가까운 큰 중단점과 동일한 너비로 다운로드되고 클라이언트에 대해 축소됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

선택 사항입니다.

## 기본값 {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## 예 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`imagereload=1,breakpoint,200;400;800;1600`
