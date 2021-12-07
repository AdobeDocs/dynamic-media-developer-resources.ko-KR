---
title: SmartCropVideoPlayer.singleclick
description: 스마트 자르기 비디오 뷰어에 대한 구성 속성입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 5%

---

# SmartCropVideoPlayer.singleclick{#smartcropvideoplayer-singleclick}

스마트 자르기 비디오 뷰어에 대한 구성 속성입니다.

` [SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]singleclick= *`none|playPause`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> none|playPause</span> </span> </p> </td> 
   <td colname="col2"> <p> 재생/일시 정지를 전환하도록 단일 클릭/탭 매핑을 구성합니다. 설정 대상 <span class="codeph"> 없음</span> 재생/일시 정지를 위해 단일 클릭/탭을 비활성화합니다. 로 설정된 경우 <span class="codeph"> playPause</span>비디오를 클릭하면 비디오 재생과 일시 중지 간에 토글됩니다. 일부 장치에서는 기본 컨트롤을 사용할 수 있습니다. 이런 경우에는 <span class="codeph"> 단일 클릭</span> 동작이 비활성화되었습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-f42369774e2740dcb399626a0e4e930e}

선택 사항입니다.

## 기본값 {#section-d016470e92a74f98a18c4ab3489410a5}

`playPause`

## 예 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
singleclick=none
```
