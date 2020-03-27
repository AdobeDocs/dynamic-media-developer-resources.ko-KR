---
description: 재생이 시작되기 전에 뷰어가 비디오 내용 로드를 시작하는지 여부를 나타냅니다.
seo-description: 재생이 시작되기 전에 뷰어가 비디오 내용 로드를 시작하는지 여부를 나타냅니다.
seo-title: VideoPlayer.preload
solution: Experience Manager
title: VideoPlayer.preload
topic: Dynamic media
uuid: 2aaae96d-d42d-4984-aec9-86e06b3c711c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# VideoPlayer.preload{#videoplayer-preload}

재생이 시작되기 전에 뷰어가 비디오 내용 로드를 시작하는지 여부를 나타냅니다.

`[VideoPlayer.|<containerId>_videoPlayer.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 1로 <span class="codeph"> 설정하면 </span> 자산이 설정된 직후에 비디오가 다운로드됩니다.그렇지 않으면 최종 사용자가 재생을 시작하거나 API 호출이 시작된 후에만 미리 로드가 시작됩니다. </p> <p>0으로 설정하면 재생이 시작될 때까지 <span class="codeph"> </span> 특정 기능이 작동하지 않을 수 있습니다.특히, 검색 작업은 비디오 프레임을 업데이트하지 않습니다. 포스터 이미지가 비활성화된 경우 뷰어는 첫 번째 비디오 프레임 대신 빈 영역으로 표시됩니다. </p> <p>특정 버전의 Internet Explorer 11 및 Edge 브라우저에서는 비디오 미리 로드 비활성화가 무시될 수 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택 사항입니다.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
