---
title: VideoPlayer.playback
description: 혼합 미디어 비디오 뷰어에 대한 구성 속성입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: accf2b56-d7bd-483d-9759-fa38246a0a8f
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 2%

---

# VideoPlayer.playback{#videoplayer-playback}

혼합 미디어 비디오 뷰어에 대한 구성 속성입니다.

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_27B4B2DDD44D4D1CB46DD1906A92B2FD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 자동|점진적</span> </p> </td> 
   <td colname="col2"> <p> 뷰어에서 사용하는 재생 유형을 설정합니다. <span class="codeph"> auto</span>이(가) 설정되면 대부분의 데스크톱 브라우저와 모든 iOS 장치에서 뷰어는 HLS 형식의 HTML5 스트리밍 비디오를 사용합니다. 이전 Internet Explorer 및 Android™과 같은 특정 시스템에서 점진적 HTML5 재생으로 후퇴합니다. </p> <p><span class="codeph"> progressive</span>이(가) 지정된 경우 뷰어는 브라우저에서 기본적으로 지원하는 HTML5 재생에만 의존하며 모든 시스템에서 점진적으로 비디오를 재생합니다. </p> <p>자동 및 점진적 모드에서 재생 선택에 대한 자세한 내용은 Viewer SDK 사용 안내서를 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택적.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`auto`

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`playback=progressive`
