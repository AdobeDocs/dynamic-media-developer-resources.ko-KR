---
title: VideoPlayer.preload
description: 재생이 시작되기 전에 뷰어가 비디오 컨텐츠 로드를 시작하는지 여부를 나타냅니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: afabbfde-e003-4fee-a4ef-0fc4c43fd960
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 4%

---

# VideoPlayer.preload{#videoplayer-preload}

재생이 시작되기 전에 뷰어가 비디오 컨텐츠 로드를 시작하는지 여부를 나타냅니다.

`[VideoPlayer.|<containerId>_videoPlayer.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 1 </span> 로 설정하면 자산이 설정된 직후에 비디오가 다운로드되기 시작합니다. 그렇지 않으면 최종 사용자가 재생을 시작하거나 API 호출에 의해 시작된 후에만 사전 로드가 시작됩니다. </p> <p><span class="codeph"> 0 </span> 로 설정하면 재생이 시작될 때까지 특정 기능이 작동하지 않을 수 있습니다. 특히 찾기 작업은 비디오 프레임을 업데이트하지 않습니다. 포스터 이미지가 비활성화되면 뷰어는 첫 번째 비디오 프레임 대신 빈 영역으로 표시됩니다. </p> <p>Internet Explorer 11 및 Edge 브라우저의 특정 버전에서 비디오 미리 로드를 사용하지 않도록 설정하는 것은 무시할 수 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택 사항입니다.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
