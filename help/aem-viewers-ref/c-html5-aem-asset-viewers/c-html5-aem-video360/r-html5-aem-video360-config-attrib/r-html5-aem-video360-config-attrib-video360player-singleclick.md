---
title: Video360Player.singleclick
description: Video360 뷰어에 대한 구성 속성입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: dfb44ed5-5f4f-4a2c-a3b4-d49502556399
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 4%

---

# Video360Player.singleclick{#video-player-singleclick}

Video360 뷰어에 대한 구성 속성입니다.

`[Video360Player.|<containerId>_video360Player.]singleclick=none|playPause`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 없음|playPause</span> </p> </td> 
   <td colname="col2"> <p> 재생/일시 중지를 전환하기 위한 한 번의 클릭/누르기 매핑을 구성합니다. <span class="codeph"> none</span>(으)로 설정하면 한 번 클릭/탭하여 재생/일시 중지할 수 없습니다. <span class="codeph"> playPause</span>(으)로 설정하면 비디오 선택 시 비디오 재생과 일시 중지 간을 전환합니다. 일부 장치에서는 기본 컨트롤을 사용할 수 있습니다. 이 경우 <span class="codeph"> singleclick</span> 동작이 비활성화됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택적.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

`playPause`

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
singleclick=none
```
