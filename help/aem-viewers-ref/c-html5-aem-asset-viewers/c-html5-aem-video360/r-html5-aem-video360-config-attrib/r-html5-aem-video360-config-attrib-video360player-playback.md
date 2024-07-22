---
title: Video360Player.playback
description: Video360 뷰어에 대한 구성 속성입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: e5a56195-c3ca-4748-aef6-e1f143ac254d
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 1%

---

# Video360Player.playback{#video-player-playback}

Video360 뷰어에 대한 구성 속성입니다.

`[Video360Player.|<containerId>_video360Player.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 자동|점진적</span> </p> </td> 
   <td colname="col2"> <p> 뷰어에서 사용하는 재생 유형을 설정합니다. </p> <p><span class="codeph"> auto</span>이(가) 설정되면 대부분의 데스크톱 브라우저 및 모든 iOS 장치에서 뷰어는 HLS 형식의 HTML5 스트리밍 비디오를 사용합니다. 또한 이전 Internet Explorer 및 Android™과 같은 특정 시스템에서 점진적 HTML5 재생으로 후퇴합니다. </p> <p><span class="codeph"> progressive</span>이(가) 설정되면 뷰어는 브라우저에서 기본적으로 지원하는 HTML5 재생에만 의존하며 모든 시스템에서 점진적으로 비디오를 재생합니다. </p> <p><span class="codeph"> 자동</span> 및 <span class="codeph"> 점진적</span> 기본 모드에서 재생 선택에 대한 자세한 내용은 HTML5 Viewers SDK 사용 안내서를 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택 사항입니다. 뷰어가 외부 비디오로 작동하는 경우 무시됩니다.

자세한 내용은 [외부 비디오 지원](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-external-video-support.md#concept-66aa2784f2294794989bad2af74c3760)을 참조하세요.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

`auto`

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`playback=progressive`
