---
description: 비디오 뷰어에 대한 구성 속성입니다.
seo-description: 비디오 뷰어에 대한 구성 속성입니다.
seo-title: VideoPlayer.singleclick
solution: Experience Manager
title: VideoPlayer.singleclick
topic: Dynamic media
uuid: df669b2e-31da-4de0-b480-e54402c9545c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 5%

---


# VideoPlayer.singleclick{#videoplayer-singleclick}

비디오 뷰어에 대한 구성 속성입니다.

` [VideoPlayer.|<containerId>_videoPlayer.]singleclick= *`none|playPause`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> none|playPause</span> </span> </p> </td> 
   <td colname="col2"> <p> 재생/일시 중지를 전환하도록 한 번의 클릭/탭 매핑을 구성합니다. <span class="codeph"> none</span>으로 설정하면 재생/일시 정지하기 위해 한 번의 클릭/탭을 사용할 수 없습니다. <span class="codeph"> playPause</span>로 설정된 경우 비디오를 클릭하면 비디오 재생과 일시 중지 간에 전환됩니다. 일부 장치에서는 기본 컨트롤을 사용할 수 있습니다. 이 경우 <span class="codeph"> singlick</span> 비헤이비어가 비활성화됩니다. </p> </td> 
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

