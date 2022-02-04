---
title: VideoScrubber.timepattern
description: 비디오 뷰어에 대한 구성 속성입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: e0956a0b-4d82-475f-8990-8b059014233a
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 3%

---

# VideoScrubber.timepattern{#videoscrubber-timepattern}

비디오 뷰어에 대한 구성 속성입니다.

`[VideoScrubber.|<containerId>_videoScrubber.]timepattern=[h:]m|mm:s|ss`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> 시간 버블에 표시되는 시간에 대한 패턴을 설정합니다. 여기서 <span class="codeph"> h</span> 시간 <span class="codeph"> m</span> 은 분입니다. 및 <span class="codeph"> s</span> 는 초입니다. </p> <p>각 시간 단위에 사용되는 글자 수는 단위에 표시할 자릿수를 결정합니다. 숫자가 지정된 자릿수에 맞지 않으면 해당 값이 후속 단위에 표시됩니다. </p> <p>예를 들어 현재 동영상 시간이 67분 5초이면 시간 패턴입니다 <span class="codeph"> m:ss</span> 는 67:05로 표시됩니다. 동일한 시간이 1로 표시됩니다:07:지정된 시간 패턴이 <span class="codeph"> h:mm:s</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-f42369774e2740dcb399626a0e4e930e}

선택 사항입니다.

## 기본값 {#section-d016470e92a74f98a18c4ab3489410a5}

`m:ss`

## 예 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
timepattern=h:mm:ss
```
