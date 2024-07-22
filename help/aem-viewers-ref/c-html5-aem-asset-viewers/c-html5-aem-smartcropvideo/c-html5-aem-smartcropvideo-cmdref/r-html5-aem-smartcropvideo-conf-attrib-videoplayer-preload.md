---
title: SmartCropVideoPlayer.preload
description: 재생이 시작되기 전에 뷰어가 비디오 컨텐츠 로드를 시작할지 여부를 나타냅니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 7a83a02e-7b75-4f15-b8c1-aa7b64e6d3bd
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 2%

---

# SmartCropVideoPlayer.preload{#smartcropvideoplayer-preload}

재생이 시작되기 전에 뷰어가 비디오 컨텐츠 로드를 시작할지 여부를 나타냅니다.

`[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 1 </span>(으)로 설정하면 자산이 설정된 직후 비디오가 다운로드되기 시작합니다. 그렇지 않으면 최종 사용자 또는 API 호출에 의해 재생이 시작된 후에만 미리 로드가 시작됩니다. </p> <p><span class="codeph"> 0 </span>(으)로 설정하면 재생이 다시 시작될 때까지 특정 기능이 작동하지 않을 수 있습니다. 특히 검색 작업은 비디오 프레임을 업데이트하지 않습니다. 포스터 이미지가 비활성화된 경우 뷰어는 첫 번째 비디오 프레임 대신 빈 영역으로 표시됩니다. </p> <p>특정 버전의 Internet Explorer 11 및 Edge 브라우저에서는 비디오 미리 로드 비활성화가 무시될 수 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택적.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
