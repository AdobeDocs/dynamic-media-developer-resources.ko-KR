---
title: SmartCropVideoPlayer.initialbitrate
description: 스마트 자르기 비디오 뷰어에 대한 구성 속성입니다.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 4fc4fefa-b094-4e2e-b8ec-a439f8a1a56c
TQID: 'https://experienceleague.adobe.com/28EPvFEtw-wS3EhTuDHpTWO1wksSmLnrKfwNJVRkFk4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 112
ht-degree: 2%

---

# SmartCropVideoPlayer.initialbitrate{#smartcropvideoplayer-initialbitrate}

비디오 뷰어에 대한 구성 속성입니다.

` [SmartCropVideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`값`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 값 </span> </p> </td> 
   <td colname="col2"> <p>데스크탑에서 비디오의 초기 재생에 사용되는 비디오 비트율(초당 킬로비트 또는 kbps)을 설정합니다. </p> <p>이 비트율 값이 응용 비디오 세트에 없으면 비디오 플레이어는 비트율이 다음으로 낮은 비디오를 시작합니다. </p> <p><span class="codeph"> 0 </span>(으)로 설정된 경우 비디오 플레이어가 가능한 가장 낮은 비트율부터 시작됩니다. HTML5 HLS 비디오(Windows 10의 Firefox, Chrome 및 Internet Explorer 11 브라우저)에 대한 기본 지원이 없는 시스템과 재생 모드가 <span class="codeph"> 자동 </span>(으)로 설정된 경우에만 적용할 수 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-f42369774e2740dcb399626a0e4e930e}

선택적.

## 기본값 {#section-d016470e92a74f98a18c4ab3489410a5}

`1400`

## 예 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
initialbitrate=600
```
