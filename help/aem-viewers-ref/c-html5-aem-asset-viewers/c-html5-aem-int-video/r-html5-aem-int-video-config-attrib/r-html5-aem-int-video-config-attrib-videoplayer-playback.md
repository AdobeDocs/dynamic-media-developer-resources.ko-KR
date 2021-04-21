---
description: 대화형 비디오 뷰어에 대한 구성 속성입니다.
solution: Experience Manager
title: VideoPlayer.playback
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,Business Practitioner
exl-id: fa49e025-1a46-4be7-ad1e-eda3b31bdc8d
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 3%

---

# VideoPlayer.playback{#videoplayer-playback}

대화형 비디오 뷰어에 대한 구성 속성입니다.

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 자동|점진적</span> </p> </td> 
   <td colname="col2"> <p> 뷰어에서 사용하는 재생 유형을 설정합니다. </p> <p><span class="codeph"> 자동</span>이 설정되면 대부분의 데스크탑 브라우저와 모든 iOS 장치에서 뷰어는 HLS 형식의 HTML5 스트리밍 비디오를 사용하고 이전 Internet Explorer 및 Android와 같은 특정 시스템에서 점진적 HTML5 재생으로 돌아갑니다. </p> <p><span class="codeph"> 점진적</span>이 설정되면 뷰어는 브라우저에서 기본적으로 지원되는 HTML5 재생에만 의존하며 모든 시스템에서 점진적으로 비디오를 재생합니다. </p> <p><span class="codeph"> auto</span> 및 <span class="codeph"> 점진적</span> 기본 모드의 재생 선택에 대한 자세한 내용은 HTML5 뷰어 SDK 사용 안내서를 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택 사항입니다.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

`auto`

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`playback=progressive`
