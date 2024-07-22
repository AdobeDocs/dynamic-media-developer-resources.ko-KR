---
title: VideoPlayer.singleclick
description: 비디오 뷰어에 대한 구성 속성입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 2fd83645-16d4-45ce-8fa8-d97dc254691f
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 4%

---

# VideoPlayer.singleclick{#videoplayer-singleclick}

비디오 뷰어에 대한 구성 속성입니다.

` [VideoPlayer.|<containerId>_videoPlayer.]singleclick= *`없음|playPause`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 없음|playPause</span> </span> </p> </td> 
   <td colname="col2"> <p> 재생/일시 중지를 전환하기 위한 한 번의 클릭/누르기 매핑을 구성합니다. <span class="codeph"> none</span>(으)로 설정하면 한 번 클릭/탭하여 재생/일시 중지할 수 없습니다. <span class="codeph"> playPause</span>(으)로 설정하면 비디오 클릭 시 비디오 재생과 일시 중지 간을 전환합니다. 일부 장치에서는 기본 컨트롤을 사용할 수 있습니다. 이 경우 <span class="codeph"> singleclick</span> 동작이 비활성화됩니다. </p> </td> 
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
