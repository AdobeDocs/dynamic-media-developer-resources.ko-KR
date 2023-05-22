---
title: VideoPlayer.iconeffect
description: 대화형 비디오 뷰어에 대한 구성 속성입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 690dc488-2db0-4166-a308-f1f3438c480a
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 3%

---

# VideoPlayer.iconeffect{#videoplayer-iconeffect}

대화형 비디오 뷰어에 대한 구성 속성입니다.

` [VideoPlayer.|<containerId>_videoPlayer.]iconeffect=0|1[, *`count`*][, *`페이드`*][, *`자동 숨기기`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> 비디오가 일시 중지된 상태일 때 비디오 맨 위에 IconEffect를 표시할 수 있도록 합니다. 일부 장치에서는 기본 컨트롤이 사용됩니다. 이러한 경우 <span class="codeph"> iconeffect</span> 수정자는 무시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 계수</span></span> </p> </td> 
   <td colname="col2"> <p> IconEffect가 나타나고 다시 나타나는 최대 횟수를 지정합니다. 값 <span class="codeph"> -1</span> 아이콘이 무한정 다시 표시됨을 나타냅니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 페이드</span></span> </p> </td> 
   <td colname="col2"> <p> 애니메이션을 표시하거나 숨기는 기간(초)을 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 자동 숨기기</span></span> </p> </td> 
   <td colname="col2"> <p> 자동으로 숨기기 전에 IconEffect가 완전히 보이는 상태를 유지하는 시간(초)을 설정합니다. 즉, 페이드 인 애니메이션이 완료된 다음 페이드 아웃 애니메이션이 시작되기 전까지의 시간입니다. 다음으로 설정 <span class="codeph"> 0</span> 자동 숨기기 동작을 비활성화합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택적.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

`1,-1,0.3,0`

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`iconeffect=0`
