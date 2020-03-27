---
description: Video360 뷰어에 대한 구성 속성입니다.
seo-description: Video360 뷰어에 대한 구성 속성입니다.
seo-title: Video360Player.playback
solution: Experience Manager
title: Video360Player.playback
topic: Dynamic media
uuid: ce814963-5cb8-408e-9d57-e7b7e61e0fab
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Video360Player.playback{#video-player-playback}

Video360 뷰어에 대한 구성 속성입니다.

`[Video360Player.|<containerId>_video360Player.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 자동|점진적</span> </p> </td> 
   <td colname="col2"> <p> 뷰어에서 사용하는 재생 유형을 설정합니다. </p> <p>대부분의 데스크탑 브라우저와 모든 iOS 장치에서 <span class="codeph"> 자동</span> 설정이 완료되면 뷰어는 HLS 형식의 HTML5 스트리밍 비디오를 사용하고 이전 Internet Explorer 및 Android와 같은 특정 시스템에서 점진적 HTML5 재생으로 돌아갑니다. </p> <p>점진적 <span class="codeph"></span> 설정이 설정되면 뷰어는 브라우저에서 기본적으로 지원되는 HTML5 재생에만 의존하며 모든 시스템에서 비디오를 점진적으로 재생합니다. </p> <p>자동 <span class="codeph"> 및</span> 점진적 <span class="codeph"></span> 기본 모드의 재생 선택에 대한 자세한 내용은 HTML5 뷰어 SDK 사용 안내서를 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택 사항입니다. 뷰어가 외부 비디오에서 작동하면 무시됩니다.

자세한 [내용은 외부 비디오 지원을](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-external-video-support.md#concept-66aa2784f2294794989bad2af74c3760) 참조하십시오.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

`auto`

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`playback=progressive`
