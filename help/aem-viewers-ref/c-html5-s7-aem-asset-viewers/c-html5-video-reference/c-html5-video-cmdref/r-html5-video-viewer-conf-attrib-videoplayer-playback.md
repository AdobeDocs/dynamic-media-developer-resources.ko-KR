---
description: 비디오 뷰어에 대한 구성 속성입니다.
seo-description: 비디오 뷰어에 대한 구성 속성입니다.
seo-title: VideoPlayer.playback
solution: Experience Manager
title: VideoPlayer.playback
topic: Dynamic media
uuid: 5ab7a322-9de0-4a26-95be-b9b2ff8e5a84
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# VideoPlayer.playback{#videoplayer-playback}

비디오 뷰어에 대한 구성 속성입니다.

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 자동|점진적</span> </p> </td> 
   <td colname="col2"> <p> 뷰어에서 사용하는 재생 유형을 설정합니다. 대부분의 데스크탑 브라우저와 모든 iOS 장치에서 <span class="codeph"> 자동이</span> 설정되면 뷰어는 HLS 형식의 HTML5 스트리밍 비디오를 사용합니다. 이전 Internet Explorer 및 Android와 같은 특정 시스템에서 점진적 HTML5 재생을 수행할 수 있습니다. </p> <p>점진적 <span class="codeph"></span> 설정이 지정되면 뷰어는 브라우저에서 기본적으로 지원되는 HTML5 재생에만 의존하며 모든 시스템에서 비디오를 점진적으로 재생합니다. </p> <p>자동 및 점진적 모드의 재생 선택에 대한 자세한 내용은 Viewer SDK 사용 안내서를 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-f42369774e2740dcb399626a0e4e930e}

선택 사항입니다.

뷰어가 외부 비디오에서 작동하면 무시됩니다. 외부 [비디오 지원을 참조하십시오](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3).

## 기본값 {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## 예 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
playback=progressive
```

