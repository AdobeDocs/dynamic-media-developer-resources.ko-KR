---
description: 대화형 비디오 뷰어에 대한 구성 속성입니다.
seo-description: 대화형 비디오 뷰어에 대한 구성 속성입니다.
seo-title: VideoTime.timepattern
solution: Experience Manager
title: VideoTime.timepattern
topic: Dynamic media
uuid: 90d36f73-44f9-4e4e-9ad6-e866749f9b2f
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# VideoTime.timepattern{#videotime-timepattern}

대화형 비디오 뷰어에 대한 구성 속성입니다.

`[VideoTime.|<containerId>_videoTime.]timepattern=[h:]m|mm:s|ss`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> 컨트롤 막대에 표시되는 시간의 패턴을 설정합니다. 여기서 <span class="codeph"> h는</span> 시간, <span class="codeph"> m</span> (분), <span class="codeph"> s</span> (초)를나타냅니다. </p> <p>각 시간 단위에 사용되는 문자 수는 해당 단위에 대해 표시할 자릿수를 결정합니다. 해당 숫자가 지정된 숫자에 맞지 않으면 해당 값이 다음 단위에 표시됩니다. </p> <p>예를 들어 현재 무비 시간이 67분 5초인 경우 <span class="codeph"> m:ss의</span> 시간 패턴이 67:05로 표시됩니다. 시간 패턴이 <span class="codeph"> h:mm:s인 경우 동일한 시간이 1:07:5로 표시됩니다</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택 사항입니다.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

`m:ss`

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
timepattern=h:mm:ss
```

