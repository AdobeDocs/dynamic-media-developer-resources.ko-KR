---
title: EmbedShare.embedsizes
description: 스마트 자르기 비디오 뷰어에 대한 구성 속성입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: c638d9fd-39bb-4baa-9b3a-99d9bc0307b5
source-git-commit: 8c49595fe0efb684b59601fb268bd8bf97fae555
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 4%

---

# EmbedShare.embedsizes{#embedshare-embedsizes}

스마트 자르기 비디오 뷰어에 대한 구성 속성입니다.

` [EmbedShare.|<containerId>_embedShare.]embedsizes= *`너비`*, *`높이`*[,0|1][; *`너비`*, *`높이`*[,0|1]]`

포함 공유 모달 대화 상자에서 크기 콤보 상자의 포함 크기 목록을 지정합니다.

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 너비 </span> </span> </p> </td> 
   <td colname="col2"> <p> 포함 폭. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 높이 </span> </span> </p> </td> 
   <td colname="col2"> <p>높이를 포함합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> 콤보 상자에서 이 목록 항목을 처음에 미리 선택할지 여부를 지정합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-f42369774e2740dcb399626a0e4e930e}

선택적.

## 기본값 {#section-d016470e92a74f98a18c4ab3489410a5}

`1280,960;640,480;320,240`

## 예 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
embedsizes=800,600;640,480,1
```
