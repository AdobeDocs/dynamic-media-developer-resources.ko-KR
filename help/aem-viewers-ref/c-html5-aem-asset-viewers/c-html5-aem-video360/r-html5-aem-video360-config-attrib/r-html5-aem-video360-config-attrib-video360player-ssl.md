---
description: Video360 뷰어에 대한 구성 속성입니다.
solution: Experience Manager
title: Video360Player.ssl
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 44efa378-c911-4449-8a10-61212d4392c6
source-git-commit: c58199c5884c368e92e50fe0ef9d6ad523e36266
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 6%

---

# Video360Player.ssl{#video-player-ssl}

Video360 뷰어에 대한 구성 속성입니다.

<!-- >[!NOTE]
>
>This configuration attribute only applies to AEM 6.2 with installation of [Feature Pack NPR-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) and to AEM 6.1 with installation of [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011). -->

`[Video360Player.|<containerId>_video360Player.]ssl=auto|on`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 자동|설정</span> </p> </td> 
   <td colname="col2"> <p> 비디오가 보안 SSL 연결(HTTPS)을 통해 전달되는지 아니면 비보안 연결(HTTP)을 통해 전달되는지를 제어합니다. </p> <p><span class="codeph"> auto</span> 로 설정하면 비디오 전달 프로토콜이 포함 웹 페이지의 프로토콜에서 상속됩니다. 웹 페이지가 HTTPS를 통해 로드되면 HTTPS를 통해 비디오도 전달되고 그 반대의 경우도 마찬가지입니다. 웹 페이지가 HTTP에 있는 경우 비디오가 HTTP를 통해 제공됩니다. </p> <p></span>에서 <span class="codeph">으로 설정하면 웹 페이지 프로토콜에 관계없이 항상 보안 연결을 통해 비디오 전달이 발생합니다. </span></p> <p>게시된 비디오 게재에만 영향을 주며 작성자 모드에서 비디오 미리 보기에 대해서는 무시됩니다. </p> </td> 
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

또한 [보안 비디오 배달](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-securevideodelivery.md#concept-13f66fdd4a52494aa516cd0f36fdac27)을 참조하십시오.
