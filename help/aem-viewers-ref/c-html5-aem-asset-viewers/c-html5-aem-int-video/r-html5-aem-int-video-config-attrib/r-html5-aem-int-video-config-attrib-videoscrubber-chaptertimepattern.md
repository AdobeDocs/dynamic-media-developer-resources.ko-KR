---
title: VideoScrubber.chaptertimepattern
description: 대화형 비디오 뷰어에 대한 구성 속성입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 93c1d38c-1f45-4794-8084-f520f9caf257
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 2%

---

# VideoScrubber.chaptertimepattern{#videoscrubber-chaptertimepattern}

대화형 비디오 뷰어에 대한 구성 속성입니다.

`[VideoScrubber.|<containerId>_videoScrubber.]chaptertimepattern=[h:]m|mm:s|ss`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> 장 레이블의 제목 표시줄에 표시되는 시간 패턴을 설정합니다. 여기서 <span class="codeph">h</span>은(는) 시간을 나타내고 <span class="codeph">m</span>은(는) 분을 나타내고 <span class="codeph">s</span>은(는) 초를 나타냅니다. </p> <p>각 시간 단위에 사용되는 문자 수는 단위에 대해 표시할 자릿수를 결정합니다. 숫자가 지정된 자릿수와 맞지 않으면 동등한 값이 후속 단위에 표시됩니다. </p> <p>예를 들어 현재 동영상 시간이 67분 5초이면 시간 패턴 <span class="codeph">m:ss</span>이(가) 67:05로 표시됩니다. 시간 패턴이 <span class="codeph">시간:mm:초</span>인 경우 동일한 시간이 1:07:5로 표시됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택적.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

`m:ss`

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
chaptertimepattern=h:mm:ss
```
