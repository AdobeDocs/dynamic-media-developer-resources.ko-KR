---
description: 대화형 비디오 뷰어에 대한 구성 속성입니다.
seo-description: 대화형 비디오 뷰어에 대한 구성 속성입니다.
seo-title: VideoScrubber.timepattern
solution: Experience Manager
title: VideoScrubber.timepattern
topic: Dynamic media
uuid: dc2e7b18-abd7-4b53-a0c4-268ec9cf3cb4
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---


# VideoScrubber.timepattern{#videoscrubber-timepattern}

대화형 비디오 뷰어에 대한 구성 속성입니다.

`[VideoScrubber.|<containerId>_videoScrubber.]timepattern=[h:]m|mm:s|ss`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> 시간 버블에 표시되는 시간의 패턴을 설정합니다. 여기서 <span class="codeph"> h</span>은 시간을, <span class="codeph"> m</span>(분) 및 <span class="codeph"> s</span>(초)을 나타냅니다. </p> <p>각 시간 단위에 사용된 문자 수는 해당 단위에 대해 표시할 자릿수를 결정합니다. 숫자가 지정된 숫자에 맞지 않을 경우, 해당 값이 후속 단위에 표시됩니다. </p> <p>예를 들어 현재 동영상 시간이 67분 5초이면 <span class="codeph"> m:ss</span>의 시간 패턴이 67:05로 표시됩니다. 시간 패턴이 <span class="codeph"> h:mm:s</span>이면 같은 시간이 1:07:5으로 표시됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택 사항입니다.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

`mm:s`

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
timepattern=h:mm:ss
```

