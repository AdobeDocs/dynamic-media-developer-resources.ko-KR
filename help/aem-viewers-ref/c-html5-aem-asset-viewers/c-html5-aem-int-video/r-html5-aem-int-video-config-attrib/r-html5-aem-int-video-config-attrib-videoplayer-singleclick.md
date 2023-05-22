---
title: VideoPlayer.singleclick
description: 대화형 비디오 뷰어에 대한 구성 속성입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 038640c7-ae8c-43e0-979b-6010bb5e40fb
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 4%

---

# VideoPlayer.singleclick{#videoplayer-singleclick}

대화형 비디오 뷰어에 대한 구성 속성입니다.

`[VideoPlayer.|<containerId>_videoPlayer.]singleclick=none|playPause`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 없음|playPause</span> </p> </td> 
   <td colname="col2"> <p> 재생/일시 중지를 전환하기 위한 한 번의 클릭/누르기 매핑을 구성합니다. 을 로 설정 <span class="codeph"> 없음</span> 한 번 클릭/탭하여 재생/일시 중지를 비활성화합니다. 로 설정된 경우 <span class="codeph"> playPause</span>를 선택한 다음 비디오를 선택하면 비디오 재생과 일시 중지 간을 전환합니다. 일부 장치에서는 기본 컨트롤을 사용할 수 있습니다. 이 경우 a <span class="codeph"> singleclick</span> 비헤이비어가 비활성화되었습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택적.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

`playPause`

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
singleclick=none
```
