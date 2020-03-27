---
description: 널
seo-description: 널
seo-title: FlyoutZoomView.imagereload
solution: Experience Manager
title: FlyoutZoomView.imagereload
topic: Dynamic media
uuid: 1de87e2f-5cb9-406a-96bc-3486c2592951
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *``*[; *`폭`*]]`

<table id="table_42CA0074AD7C4F0D9FC81E9FCB0591C0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 구성 요소가 크기 조정 중에 기본 및 플라이아웃 보기에 대한 새 이미지를 가져오는 방법을 구성합니다. </p> <p>0으로 설정하면 구성 요소가 크기 조정 <span class="codeph"> </span>중에 새 이미지를 로드하지 않습니다.플라이아웃 보기의 이미지 해상도는 변경되지 않습니다. </p> <p>1로 <span class="codeph"> </span> 설정하면 기본 보기로 로드된 이미지에 대해 하나 이상의 폭 중단점을 지정할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 중단점, <span class="varname"> 폭 </span>[; <span class="varname"> 너비 </span>] </span> </p> </td> 
   <td colname="col2"> <p> 기본 보기로 로드되는 이미지의 폭 중단점입니다. 구성 요소는 항상 초기 로드에 가장 적합한 크기를 사용합니다. 크기를 조정하면 기본 보기의 이미지가 항상 가장 큰 중단점과 같은 너비로 다운로드되고 클라이언트에서 축소됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

선택 사항입니다.

## 기본값 {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## 예 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`imagereload=1,breakpoint,200;400;800;1600`
