---
description: 혼합 미디어 비디오 뷰어에 대한 구성 속성입니다.
seo-description: 혼합 미디어 비디오 뷰어에 대한 구성 속성입니다.
seo-title: VideoPlayer.playback
solution: Experience Manager
title: VideoPlayer.playback
topic: Dynamic media
uuid: 7016d414-aa93-4854-8f95-24e94082b5ce
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 3%

---


# VideoPlayer.playback{#videoplayer-playback}

혼합 미디어 비디오 뷰어에 대한 구성 속성입니다.

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_27B4B2DDD44D4D1CB46DD1906A92B2FD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 자동|점진적</span> </p> </td> 
   <td colname="col2"> <p> 뷰어에서 사용하는 재생 유형을 설정합니다. <span class="codeph"> auto</span>이 설정되면 대부분의 데스크탑 브라우저와 모든 iOS 장치에서 뷰어는 HLS 형식의 HTML5 스트리밍 비디오를 사용합니다. 이전 Internet Explorer 및 Android와 같은 특정 시스템에서 점진적 HTML5 재생을 지원합니다. </p> <p><span class="codeph"> 점진적</span>이 지정된 경우 뷰어는 브라우저에서 기본적으로 지원되는 HTML5 재생에만 의존하며 모든 시스템에서 점진적으로 비디오를 재생합니다. </p> <p>자동 및 점진적 모드의 재생 선택에 대한 자세한 내용은 뷰어 SDK 사용 안내서를 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택 사항입니다.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`auto`

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`playback=progressive`
