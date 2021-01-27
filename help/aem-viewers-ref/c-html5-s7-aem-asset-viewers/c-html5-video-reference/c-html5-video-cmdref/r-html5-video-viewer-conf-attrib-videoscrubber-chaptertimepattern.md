---
description: 비디오 뷰어에 대한 구성 속성입니다.
seo-description: 비디오 뷰어에 대한 구성 속성입니다.
seo-title: VideoScrubber.chaptertimepattern
solution: Experience Manager
title: VideoScrubber.chaptertimepattern
topic: Dynamic Media
uuid: 75338fa6-83ab-4cb8-babf-e958f97c1b6e
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---


# VideoScrubber.chaptertimepattern{#videoscrubber-chaptertimepattern}

비디오 뷰어에 대한 구성 속성입니다.

`[VideoScrubber.|<containerId>_videoScrubber.]chaptertimepattern=[h:]m|mm:s|ss`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> 비디오 장 레이블의 제목 표시줄에 표시되는 시간의 패턴을 설정합니다. 여기서 <span class="codeph"> h</span>은 시간, <span class="codeph"> m</span>은 분, <span class="codeph">의 </span>는 초입니다. </p> <p>각 시간 단위에 사용된 문자 수는 해당 단위에 대해 표시할 자릿수를 결정합니다. 숫자가 지정된 숫자에 맞지 않을 경우, 해당 값이 후속 단위에 표시됩니다. </p> <p>예를 들어 현재 동영상 시간이 67분 5초이면 시간 패턴 <span class="codeph"> m:ss</span>이 67:05로 표시됩니다. 지정된 시간 패턴이 <span class="codeph"> h:mm:s</span>인 경우 같은 시간이 1:07:5으로 표시됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-f42369774e2740dcb399626a0e4e930e}

선택 사항입니다.

## 기본값 {#section-d016470e92a74f98a18c4ab3489410a5}

`m:ss`

## 예 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
chaptertimepattern=h:mm:ss
```

