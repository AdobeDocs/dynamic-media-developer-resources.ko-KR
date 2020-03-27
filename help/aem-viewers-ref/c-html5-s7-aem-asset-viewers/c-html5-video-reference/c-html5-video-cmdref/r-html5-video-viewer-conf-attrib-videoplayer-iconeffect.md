---
description: 비디오 뷰어에 대한 구성 속성입니다.
seo-description: 비디오 뷰어에 대한 구성 속성입니다.
seo-title: VideoPlayer.iconeffect
solution: Experience Manager
title: VideoPlayer.iconeffect
topic: Dynamic media
uuid: 1ba6f24a-77bb-41ef-a831-a7ac817abd73
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# VideoPlayer.iconeffect{#videoplayer-iconeffect}

비디오 뷰어에 대한 구성 속성입니다.

` [VideoPlayer.|<containerId>_videoPlayer.]iconeffect= *`0|1`*[, *``*][, *``*][, *`countrfadeautoHide`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 0|1</span> </span> </p> </td> 
   <td colname="col2"> <p> 비디오가 일시 중지되면 IconEffect가 비디오 위에 표시되도록 합니다. 일부 장치에서는 기본 컨트롤이 사용됩니다. 이 경우 <span class="codeph"> iconeffect</span> 수정자는 무시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 카운트</span></span> </p> </td> 
   <td colname="col2"> <p> IconEffect가 표시되고 다시 표시되는 최대 횟수를 지정합니다. 값이 <span class="codeph"> -1</span> 이면 아이콘이 무기한 다시 나타납니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 페이드</span></span> </p> </td> 
   <td colname="col2"> <p> 애니메이션을 표시하거나 숨기는 지속 시간(초)을 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 자동 <span class="varname"> 숨기기</span></span> </p> </td> 
   <td colname="col2"> <p> IconEffect가 자동 숨김 전에 계속 표시되는 시간(초)을 설정합니다. 즉, 페이드 인 애니메이션이 완료된 후 페이드 아웃 애니메이션이 시작되기 전의 시간입니다. 0으로 설정하면 <span class="codeph"></span> 자동 숨기기 동작이 비활성화됩니다. </p> </td> 
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

