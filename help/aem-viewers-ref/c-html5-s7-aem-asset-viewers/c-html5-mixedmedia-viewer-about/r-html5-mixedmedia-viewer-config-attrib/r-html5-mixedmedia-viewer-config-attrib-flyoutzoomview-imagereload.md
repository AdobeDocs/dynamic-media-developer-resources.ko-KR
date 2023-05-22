---
title: FlyoutZoomView.imagereload
description: 구성 요소가 크기 변경 중 기본 및 플라이아웃 보기에 대한 새 이미지를 가져오는 방법을 구성합니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 1bb57c89-4ceb-40d6-8054-d51c1573431c
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 3%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

구성 요소가 크기 변경 중 기본 및 플라이아웃 보기에 대한 새 이미지를 가져오는 방법을 구성합니다.

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *`폭`*[; *`폭`*]]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p>로 설정된 경우 <span class="codeph"> 0 </span>, 구성 요소는 크기 변경 중 새 이미지를 로드하지 않고 플라이아웃 보기의 이미지 해상도가 변경되지 않습니다. </p> <p>로 설정된 경우 <span class="codeph"> 1 </span> 기본 보기에 로드되는 이미지에 대해 하나 이상의 너비 중단점을 지정할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 중단점, <span class="varname"> 폭 </span>[; <span class="varname"> 폭 </span>] </span> </p> </td> 
   <td colname="col2"> <p>기본 보기에 로드되는 이미지의 너비 중단점입니다. 구성 요소는 항상 초기 로드에 가장 적합한 크기를 사용합니다. 크기를 조정하면 기본 보기의 이미지가 항상 가장 가까운 더 큰 중단점과 동일한 너비로 다운로드되고 클라이언트에서 크기가 줄어듭니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택적.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`imagereload=1,breakpoint,200;400;800;1600`
