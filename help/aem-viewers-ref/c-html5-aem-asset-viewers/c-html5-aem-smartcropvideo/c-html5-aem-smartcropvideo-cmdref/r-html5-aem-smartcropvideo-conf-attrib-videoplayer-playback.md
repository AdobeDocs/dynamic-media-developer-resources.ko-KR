---
description: 스마트 자르기 비디오 뷰어에 대한 구성 속성입니다.
solution: Experience Manager
title: SmartCropVideoPlayer.playback
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 54a10b30-ebf5-4f1e-aa4a-b09055453c4e
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 2%

---

# SmartCropVideoPlayer.playback{#smartcropvideoplayer-playback}

스마트 자르기 비디오 뷰어에 대한 구성 속성입니다.

`[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]playback=auto|progressive`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 자동|점진적</span> </p> </td> 
   <td colname="col2"> <p> 뷰어에서 사용하는 재생 유형을 설정합니다. When <span class="codeph"> 자동</span> 이 설정되면 대부분의 데스크탑 브라우저와 모든 iOS 장치에서 뷰어는 HLS 형식의 HTML5 스트리밍 비디오를 사용합니다. 이전 Internet Explorer 및 Android와 같은 특정 시스템에서 점진적 HTML5 재생으로 돌아갑니다. </p> <p>If <span class="codeph"> 진보</span> 가 지정되면 뷰어는 브라우저가 기본적으로 지원하는 HTML5 재생에만 의존하며 모든 시스템에서 점진적으로 비디오를 재생합니다. </p> <p>자동 및 점진적 모드의 재생 선택에 대한 자세한 내용은 뷰어 SDK 사용 안내서를 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-f42369774e2740dcb399626a0e4e930e}

선택 사항입니다.

뷰어가 외부 비디오에서 작동할 때 무시됩니다. 자세한 내용은 [외부 비디오 지원]
(../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3).

## 기본값 {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## 예 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
playback=progressive
```
