---
description: 비디오 뷰어에 대한 구성 속성입니다.
solution: Experience Manager
title: VideoPlayer.iconeffect
feature: Dynamic Media Classic,Viewers,SDK/API,비디오
role: Developer,Business Practitioner
exl-id: b283b495-ee28-4f9d-ad4d-b14ac2f9a1a2
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 4%

---

# VideoPlayer.iconeffect{#videoplayer-iconeffect}

비디오 뷰어에 대한 구성 속성입니다.

` [VideoPlayer.|<containerId>_videoPlayer.]iconeffect= *`0|1`*[, *``*][, *``*][, *`countfadeautoHide`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 0|1</span> </span> </p> </td> 
   <td colname="col2"> <p> 비디오가 일시 중지되면 IconEffect가 비디오 맨 위에 표시되도록 합니다. 일부 장치에서는 기본 컨트롤이 사용됩니다. 이 경우 <span class="codeph"> iconeffect</span> 한정자는 무시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> count</span> </span> </p> </td> 
   <td colname="col2"> <p> IconEffect가 나타나고 다시 나타나는 최대 횟수를 지정합니다. <span class="codeph"> -1</span> 값은 아이콘이 무기한으로 다시 표시됨을 나타냅니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 페이드</span> </span> </p> </td> 
   <td colname="col2"> <p> 애니메이션 표시 또는 숨기기 지속 시간(초)을 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> autoHide</span> </span> </p> </td> 
   <td colname="col2"> <p> IconEffect가 자동으로 숨겨지기 전에 표시되는 시간(초)을 설정합니다. 즉, 페이드 인 애니메이션이 완료된 후 페이드 아웃 애니메이션이 시작되기 전의 시간입니다. <span class="codeph"> 0</span> 설정은 자동 숨기기 동작을 비활성화합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-f42369774e2740dcb399626a0e4e930e}

선택 사항입니다.

## 기본값 {#section-d016470e92a74f98a18c4ab3489410a5}

`1,-1,0.3,0`

## 예 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
iconeffect=0
```
