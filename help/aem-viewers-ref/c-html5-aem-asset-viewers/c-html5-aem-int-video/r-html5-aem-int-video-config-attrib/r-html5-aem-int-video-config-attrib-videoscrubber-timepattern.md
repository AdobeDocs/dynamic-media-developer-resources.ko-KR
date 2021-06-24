---
description: 대화형 비디오 뷰어에 대한 구성 속성입니다.
solution: Experience Manager
title: VideoScrubber.timepattern
feature: Dynamic Media Classic,Viewers,SDK/API,대화형 비디오
role: Developer,Business Practitioner
exl-id: d39ddf38-9157-412a-83a4-c1af4944a904
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
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
   <td colname="col2"> <p> 시간 버블에 표시되는 시간의 패턴을 설정합니다. 여기서 <span class="codeph"> h</span>은 시간을 나타내고, <span class="codeph"> m</span>은 분, <span class="codeph"> s</span>는 초 동안 설정합니다. </p> <p>각 시간 단위에 사용되는 글자 수는 단위에 표시할 자릿수를 결정합니다. 숫자가 지정된 자릿수에 맞지 않으면 해당 값이 후속 단위에 표시됩니다. </p> <p>예를 들어 현재 동영상 시간이 67분 5초인 경우 <span class="codeph"> m:ss</span>의 시간 패턴이 67:05로 표시됩니다. 시간 패턴이 <span class="codeph"> h:mm:s</span>인 경우 동일한 시간이 1:07:5로 표시됩니다. </p> </td> 
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
