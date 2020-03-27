---
description: 대화형 비디오 뷰어에 대한 구성 속성입니다.
seo-description: 대화형 비디오 뷰어에 대한 구성 속성입니다.
seo-title: VideoPlayer.iconeffect
solution: Experience Manager
title: VideoPlayer.iconeffect
topic: Dynamic media
uuid: a403d44d-d5b5-4d09-876e-39146585704f
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# VideoPlayer.iconeffect{#videoplayer-iconeffect}

대화형 비디오 뷰어에 대한 구성 속성입니다.

` [VideoPlayer.|<containerId>_videoPlayer.]iconeffect=0|1[, *``*][, *``*][, *`countfadeautoHide`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> 비디오가 일시 중지 상태일 때 비디오 상단에 IconEffect가 표시되도록 합니다. 일부 장치에서는 기본 컨트롤이 사용됩니다. 이러한 경우 iconeffect <span class="codeph"></span> 수정자는 무시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 계수</span></span> </p> </td> 
   <td colname="col2"> <p> IconEffect가 표시되고 다시 표시되는 최대 횟수를 지정합니다. 값이 <span class="codeph"> -1</span> 이면 아이콘이 무기한 다시 나타납니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 페이드</span></span> </p> </td> 
   <td colname="col2"> <p> 애니메이션을 표시하거나 숨기는 지속 시간(초)을 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p> IconEffect가 자동 숨김 전에 완전히 표시되는 시간(초)을 설정합니다. 즉, 페이드 인 애니메이션이 완료된 후 페이드 아웃 애니메이션이 시작되기 전의 시간입니다. 자동 숨기기 동작을 비활성화하려면 <span class="codeph"> 0으로</span> 설정합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택 사항입니다.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

`1,-1,0.3,0`

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`iconeffect=0`
