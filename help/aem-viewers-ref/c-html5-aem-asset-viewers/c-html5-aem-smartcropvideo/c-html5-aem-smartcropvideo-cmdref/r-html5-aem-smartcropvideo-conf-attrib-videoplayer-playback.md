---
title: SmartCropVideoPlayer.playback
description: 스마트 자르기 비디오 뷰어에 대한 구성 속성입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 6df94fe7-30ea-42f1-a39e-50219259a098
source-git-commit: 8c49595fe0efb684b59601fb268bd8bf97fae555
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 2%

---

# SmartCropVideoPlayer.playback{#smartcropvideoplayer-playback}

스마트 자르기 비디오 뷰어에 대한 구성 속성입니다.

`[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]playback=auto|progressive`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 자동|점진적</span> </p> </td> 
   <td colname="col2"> <p> 뷰어에서 사용하는 재생 유형을 설정합니다. <span class="codeph"> auto</span>이(가) 설정되면 대부분의 데스크톱 브라우저와 모든 iOS 장치에서 뷰어는 HTML5 스트리밍 비디오를 HLS 형식으로 사용합니다. 이전 Internet Explorer 및 Android™과 같은 특정 시스템에서 점진적 HTML5 재생으로 후퇴합니다. </p> <p><span class="codeph"> progressive</span>이(가) 지정된 경우 뷰어는 브라우저에서 기본적으로 지원하는 HTML5 재생에만 의존하며 모든 시스템에서 점진적으로 비디오를 재생합니다. </p> <p>자동 및 점진적 모드에서 재생 선택에 대한 자세한 내용은 뷰어 SDK 사용 안내서 를 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-f42369774e2740dcb399626a0e4e930e}

선택적.

뷰어가 외부 비디오로 작동하는 경우 무시됩니다. [외부 비디오 지원]을 참조하세요.
(../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3).

## 기본값 {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## 예 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
playback=progressive
```
