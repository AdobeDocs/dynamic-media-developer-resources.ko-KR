---
title: SmartCropVideoPlayer.singleclick
description: 스마트 자르기 비디오 뷰어에 대한 구성 속성입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: f48f0866-4eb7-46c5-a7f5-457df7a568e7
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 4%

---

# SmartCropVideoPlayer.singleclick{#smartcropvideoplayer-singleclick}

스마트 자르기 비디오 뷰어에 대한 구성 속성입니다.

` [SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]singleclick= *`없음|playPause`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 없음|playPause</span> </span> </p> </td> 
   <td colname="col2"> <p> 재생/일시 중지를 전환하기 위한 한 번의 클릭/누르기 매핑을 구성합니다. 을 로 설정 <span class="codeph"> 없음</span> 한 번 클릭/탭하여 재생/일시 중지를 비활성화합니다. 로 설정된 경우 <span class="codeph"> playPause</span>를 클릭하면 비디오 재생과 일시 중지 간을 전환합니다. 일부 장치에서는 기본 컨트롤을 사용할 수 있습니다. 이런 경우, <span class="codeph"> singleclick</span> 비헤이비어가 비활성화되었습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-f42369774e2740dcb399626a0e4e930e}

선택적.

## 기본값 {#section-d016470e92a74f98a18c4ab3489410a5}

`playPause`

## 예 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
singleclick=none
```
