---
title: VideoPlayer.iconeffect
description: 비디오 뷰어에 대한 구성 속성입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: b283b495-ee28-4f9d-ad4d-b14ac2f9a1a2
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 2%

---

# VideoPlayer.iconeffect{#videoplayer-iconeffect}

비디오 뷰어에 대한 구성 속성입니다.

` [VideoPlayer.|<containerId>_videoPlayer.]iconeffect= *`0|1`*[, *`count`*][, *`fade`*][, *`autoHide`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 0|1</span> </span> </p> </td> 
   <td colname="col2"> <p> 비디오가 일시 중지되면 비디오 위에 IconEffect를 표시할 수 있도록 합니다. 일부 장치에서는 기본 컨트롤이 사용됩니다. 이 경우 <span class="codeph"> iconeffect</span> 한정자는 무시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 개수</span> </span> </p> </td> 
   <td colname="col2"> <p> IconEffect가 나타나고 다시 나타나는 최대 횟수를 지정합니다. <span class="codeph"> -1</span> 값은 아이콘이 무기한 다시 표시됨을 나타냅니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 페이드</span> </span> </p> </td> 
   <td colname="col2"> <p> 애니메이션을 표시하거나 숨기는 기간(초)을 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 자동 숨기기</span> </span> </p> </td> 
   <td colname="col2"> <p> 자동으로 숨기기 전에 IconEffect가 보이는 상태를 유지하는 시간(초)을 설정합니다. 즉, 페이드 인 애니메이션이 완료된 다음 페이드 아웃 애니메이션이 시작되기 전까지의 시간을 의미한다. <span class="codeph"> 0</span> 설정은 자동 숨기기 동작을 사용하지 않도록 설정합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-f42369774e2740dcb399626a0e4e930e}

선택적.

## 기본값 {#section-d016470e92a74f98a18c4ab3489410a5}

`1,-1,0.3,0`

## 예 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
iconeffect=0
```
