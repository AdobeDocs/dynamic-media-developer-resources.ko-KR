---
description: 크기 조정 중에 구성 요소가 기본 및 플라이아웃 보기에 대한 새 이미지를 가져오는 방법을 구성합니다.
solution: Experience Manager
title: FlyoutZoomView.imagereload
feature: Dynamic Media Classic,Viewers,SDK/API,혼합 미디어 집합
role: Developer,Business Practitioner
exl-id: 1bb57c89-4ceb-40d6-8054-d51c1573431c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 3%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

크기 조정 중에 구성 요소가 기본 및 플라이아웃 보기에 대한 새 이미지를 가져오는 방법을 구성합니다.

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *``*[; *`너비`*]]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 0 </span> 로 설정하면 구성 요소가 크기 조정 중에 새 이미지를 로드하지 않고 플라이아웃 보기의 이미지 해상도는 변경되지 않습니다. </p> <p><span class="codeph"> 1 </span>로 설정하면 기본 보기에 로드되는 이미지에 대해 하나 이상의 너비 중단점을 지정할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 중단점,  <span class="varname"> 너비  </span>[; <span class="varname"> 너비  </span>]  </span> </p> </td> 
   <td colname="col2"> <p>기본 보기에 로드되는 이미지의 너비 중단점. 구성 요소는 항상 초기 로드에 가장 적합한 크기를 사용합니다. 크기를 조정하면 기본 보기의 이미지가 항상 가장 가까운 더 큰 중단점과 동일한 너비로 다운로드되고 클라이언트에 대해 축소됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택 사항입니다.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`imagereload=1,breakpoint,200;400;800;1600`
