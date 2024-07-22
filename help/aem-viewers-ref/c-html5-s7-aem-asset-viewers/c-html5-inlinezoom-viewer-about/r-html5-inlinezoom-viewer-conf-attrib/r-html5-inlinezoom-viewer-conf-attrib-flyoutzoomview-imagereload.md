---
title: FlyoutZoomView.imagereload
description: FlyoutZoomView.imagereload
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 84dd1e40-2ab8-4356-9eff-8766432b539b
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 2%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *`너비`*[; *`너비`*]]`

<table id="table_7DA232CB62134078B788B9AB1452F363"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> 구성 요소가 크기 변경 중 기본 및 플라이아웃 보기에 대한 새 이미지를 가져오는 방법을 구성합니다. </p> <p><span class="codeph"> 0 </span>(으)로 설정하면 구성 요소가 크기 조정 중 새 이미지를 로드하지 않고 플라이아웃 보기의 이미지 해상도가 변경되지 않습니다. </p> <p><span class="codeph"> 1 </span>(으)로 설정하면 기본 보기에 로드한 이미지에 대해 하나 이상의 너비 중단점을 지정할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 중단점, <span class="varname"> 너비 </span>, <span class="varname"> 너비 </span> </span> </p> </td> 
   <td colname="col2"> <p>기본 보기에 로드되는 이미지의 너비 중단점입니다. </p> <p>구성 요소는 항상 초기 로드에 가장 적합한 크기를 사용합니다. 크기를 조정하면 기본 보기의 이미지가 항상 가장 가까운 더 큰 중단점과 동일한 너비를 사용하여 다운로드되고 클라이언트에서 다운스케일됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-e6310c8c4e8547689a5b48ceddb3671d}

선택적.

## 기본값 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`1,breakpoint,300;600;1200`

## 예 {#section-3a188ab955c445bcb2efa3c49722c10d}

`imagereload=1,breakpoint,200;400;800;1600`
