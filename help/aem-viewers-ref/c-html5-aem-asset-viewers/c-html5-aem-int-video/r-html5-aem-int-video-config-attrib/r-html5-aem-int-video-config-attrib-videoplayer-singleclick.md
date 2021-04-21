---
description: 대화형 비디오 뷰어에 대한 구성 속성입니다.
solution: Experience Manager
title: VideoPlayer.singleclick
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,Business Practitioner
exl-id: 038640c7-ae8c-43e0-979b-6010bb5e40fb
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 4%

---

# VideoPlayer.singleclick{#videoplayer-singleclick}

대화형 비디오 뷰어에 대한 구성 속성입니다.

`[VideoPlayer.|<containerId>_videoPlayer.]singleclick=none|playPause`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|playPause</span> </p> </td> 
   <td colname="col2"> <p> 재생/일시 중지를 전환하도록 한 번의 클릭/탭 매핑을 구성합니다. <span class="codeph"> none</span>으로 설정하면 재생/일시 정지하기 위해 한 번의 클릭/탭을 사용할 수 없습니다. <span class="codeph"> playPause</span>로 설정된 경우 비디오를 클릭하면 비디오 재생과 일시 중지 간에 전환됩니다. 일부 장치에서는 기본 컨트롤을 사용할 수 있습니다. 이 경우 <span class="codeph"> singlick</span> 비헤이비어가 비활성화됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택 사항입니다.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

`playPause`

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
singleclick=none
```
