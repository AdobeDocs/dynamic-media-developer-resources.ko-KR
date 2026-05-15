---
title: FlyoutZoomView.imagereload
description: FlyoutZoomView.imagereload
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 483fa64b-5196-4477-8ea6-0f32c6557f72
TQID: 'https://experienceleague.adobe.com/nkYQwtTb1AUBLBbnN2HwMZLIjyolj5l-6CxEy-yEo3k'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 120
ht-degree: 4%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *`너비`*[; *`너비`*]]`

<table id="table_42CA0074AD7C4F0D9FC81E9FCB0591C0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> 구성 요소가 크기 변경 중 기본 및 플라이아웃 보기에 대한 새 이미지를 가져오는 방법을 구성합니다. </p> <p><span class="codeph"> 0 </span>(으)로 설정된 경우 구성 요소는 크기 조정 중 새 이미지를 로드하지 않고, 플라이아웃 보기의 이미지 해상도가 변경되지 않습니다. </p> <p><span class="codeph"> 1 </span>(으)로 설정하면 기본 보기에 로드한 이미지에 대해 하나 이상의 너비 중단점을 지정할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 중단점, <span class="varname"> 너비 </span>[; <span class="varname"> 너비 </span>] </span> </p> </td> 
   <td colname="col2"> <p> 기본 보기에 로드되는 이미지의 너비 중단점입니다. 구성 요소는 항상 초기 로드에 가장 적합한 크기를 사용합니다. 크기를 조정하면 기본 보기의 이미지가 항상 가장 가까운 더 큰 중단점과 동일한 너비로 다운로드되고 클라이언트에서 크기가 줄어듭니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

선택적.

## 기본값 {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## 예 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`imagereload=1,breakpoint,200;400;800;1600`
