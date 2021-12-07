---
title: SmartCropVideoPlayer.ssl
description: 스마트 자르기 비디오 뷰어에 대한 구성 속성입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 3%

---

# SmartCropVideoPlayer.ssl{#smartcropvideoplayer-ssl}

스마트 자르기 비디오 뷰어에 대한 구성 속성입니다.

<!-- >[!NOTE]
>
>This configuration attribute only applies to AEM 6.2 with installation of [Feature Pack NPR-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) and to AEM 6.1 with installation of [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011). -->

`[SmartCropVideoPlayer.|<containerId>_videoPlayer.]ssl=auto|on`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 자동|설정</span> </p> </td> 
   <td colname="col2"> <p> 비디오가 보안 SSL 연결(HTTPS)을 통해 전달되는지 아니면 비보안 연결(HTTP)을 통해 전달되는지를 제어합니다. </p> <p>로 설정된 경우 <span class="codeph"> 자동</span> 비디오 전달 프로토콜은 포함 웹 페이지의 프로토콜에서 상속됩니다. 웹 페이지가 HTTPS를 통해 로드되면 비디오도 HTTPS를 통해 제공되고 반대로 전달됩니다. 웹 페이지가 HTTP에 있는 경우 비디오가 HTTP를 통해 제공됩니다. </p> <p>로 설정된 경우 <span class="codeph"> on</span>에서는 항상 웹 페이지 프로토콜에 관계없이 보안 연결을 통해 비디오를 제공합니다. </p> <p>게시된 비디오 게재에만 영향을 주며 작성자 모드에서 비디오 미리 보기에 대해서는 무시됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-f42369774e2740dcb399626a0e4e930e}

선택 사항입니다.

## 기본값 {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## 예 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
ssl=on
```

<!--<a id="section_5943AC73316749C68761FF7F74DA7547"></a>-->

참조 - [보안 비디오 제공](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-securevideodelivery.md#concept-cf9d1346a07d4429b0c6c32c9cac50ff).
