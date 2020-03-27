---
description: 비디오 뷰어에 대한 구성 속성입니다.
seo-description: 비디오 뷰어에 대한 구성 속성입니다.
seo-title: VideoScrubber.chaptertimepattern
solution: Experience Manager
title: VideoScrubber.chaptertimepattern
topic: Dynamic media
uuid: 75338fa6-83ab-4cb8-babf-e958f97c1b6e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# VideoScrubber.chaptertimepattern{#videoscrubber-chaptertimepattern}

비디오 뷰어에 대한 구성 속성입니다.

`[VideoScrubber.|<containerId>_videoScrubber.]chaptertimepattern=[h:]m|mm:s|ss`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> 비디오 장 레이블의 제목 표시줄에 표시되는 시간 패턴을 설정합니다. 여기서 <span class="codeph"> h</span> 는 <span class="codeph"> 시간,</span> m <span class="codeph"> 은 분,</span> s는초입니다. </p> <p>각 시간 단위에 사용되는 문자 수는 해당 단위에 대해 표시할 자릿수를 결정합니다. 해당 숫자가 지정된 숫자에 맞지 않으면 해당 값이 다음 단위에 표시됩니다. </p> <p>예를 들어 현재 동영상 시간이 67분 5초인 경우 시간 패턴 <span class="codeph"> m:ss</span> 는 67:05로 표시됩니다. 주어진 시간 패턴이 <span class="codeph"> h:mm:s인 경우 동일한 시간이 1:07:5로 표시됩니다</span>. </p> </td> 
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

