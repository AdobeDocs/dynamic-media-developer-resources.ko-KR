---
description: Video360 뷰어에 대한 구성 속성입니다.
solution: Experience Manager
title: EmbedShare.embedsizes
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR 비디오
role: Developer,Business Practitioner
exl-id: 3a6c23dd-5e2c-4149-aa24-37d445128125
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 10%

---

# EmbedShare.embedsizes{#embedshare-embedsizes}

Video360 뷰어에 대한 구성 속성입니다.

` [EmbedShare.|<containerId>_embedShare.]embedsizes= *``*, *``*[,0|1][; *``*, *`widthheightwidheight`*[,0|1]]`

포함 공유 모달 대화 상자에서 크기 콤보 상자의 포함 크기 목록을 지정합니다.

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> width </span> </span> </p> </td> 
   <td colname="col2"> <p> 포함 폭. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> height </span> </span> </p> </td> 
   <td colname="col2"> <p>포함 높이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 콤보 상자에서 이 목록 항목을 처음에 미리 선택할지 여부를 지정합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-f42369774e2740dcb399626a0e4e930e}

선택 사항입니다.

## 기본값 {#section-d016470e92a74f98a18c4ab3489410a5}

`1280,960;640,480;320,240`

## 예 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
embedsizes=800,600;640,480,1
```
