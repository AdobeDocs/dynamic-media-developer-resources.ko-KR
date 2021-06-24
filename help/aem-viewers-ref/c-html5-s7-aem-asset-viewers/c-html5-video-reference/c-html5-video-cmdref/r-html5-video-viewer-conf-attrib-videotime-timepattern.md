---
description: 비디오 뷰어에 대한 구성 속성입니다.
solution: Experience Manager
title: VideoTime.timepattern
feature: Dynamic Media Classic,Viewers,SDK/API,비디오
role: Developer,Business Practitioner
exl-id: 1fe2876c-c59a-4e0c-b429-34cc3244d920
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 3%

---

# VideoTime.timepattern{#videotime-timepattern}

비디오 뷰어에 대한 구성 속성입니다.

`[VideoTime.|<containerId>_videoTime.]timepattern=[h:]m|mm:s|ss`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> h</span>이 시간이고, <span class="codeph"> m</span>이 분이고, <span class="codeph"> s</span>가 초인 제어 표시줄에 표시되는 시간의 패턴을 설정합니다. </p> <p>각 시간 단위에 사용되는 글자 수는 단위에 표시할 자릿수를 결정합니다. 숫자가 지정된 자릿수에 맞지 않으면 해당 값이 후속 단위에 표시됩니다. </p> <p>예를 들어 현재 동영상 시간이 67분 5초인 경우 시간 패턴 <span class="codeph"> m:ss</span>은 67:05로 표시됩니다. 지정된 시간 패턴이 <span class="codeph"> h:mm:s</span>인 경우 동일한 시간이 1:07:5로 표시됩니다. </p> </td> 
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
