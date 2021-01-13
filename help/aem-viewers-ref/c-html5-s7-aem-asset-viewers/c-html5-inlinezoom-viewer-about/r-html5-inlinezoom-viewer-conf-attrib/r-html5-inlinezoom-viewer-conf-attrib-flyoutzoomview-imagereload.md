---
description: FlyoutZoomView.imagereload
solution: Experience Manager
title: FlyoutZoomView.imagereload
topic: Dynamic media
uuid: 98a84ba1-4b89-424a-ac2e-4a59af33cec0
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 4%

---


# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *``*[; *`폭`*]]`

<table id="table_7DA232CB62134078B788B9AB1452F363"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 구성 요소가 크기 조정 중에 기본 및 플라이아웃 보기에 대한 새 이미지를 가져오는 방법을 구성합니다. </p> <p><span class="codeph"> 0 </span>으로 설정하면 구성 요소가 크기 조정 중에 새 이미지를 로드하지 않고 플라이아웃 보기의 이미지 해상도는 변경되지 않습니다. </p> <p><span class="codeph"> 1 </span>으로 설정하면 기본 보기로 로드된 이미지에 대해 하나 이상의 폭 중단점을 지정할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 중단점,  <span class="varname"> 너비  </span>; <span class="varname"> 너비  </span> </span> </p> </td> 
   <td colname="col2"> <p>기본 보기로 로드된 이미지의 폭 중단점입니다. </p> <p>구성 요소는 항상 초기 로드에 가장 적합한 크기를 사용합니다. 크기를 조정한 후 기본 보기의 이미지가 항상 가장 가까운 큰 중단점과 같은 폭을 사용하여 다운로드되고 클라이언트에서 축소됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-e6310c8c4e8547689a5b48ceddb3671d}

선택 사항입니다.

## 기본값 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`1,breakpoint,300;600;1200`

## 예 {#section-3a188ab955c445bcb2efa3c49722c10d}

`imagereload=1,breakpoint,200;400;800;1600`
