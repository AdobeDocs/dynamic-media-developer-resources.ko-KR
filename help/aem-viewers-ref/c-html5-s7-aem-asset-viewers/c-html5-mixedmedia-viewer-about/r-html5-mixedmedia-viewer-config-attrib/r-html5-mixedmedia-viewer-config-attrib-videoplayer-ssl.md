---
description: 혼합 미디어 비디오 뷰어에 대한 구성 속성입니다.
seo-description: 혼합 미디어 비디오 뷰어에 대한 구성 속성입니다.
seo-title: VideoPlayer.ssl
solution: Experience Manager
title: VideoPlayer.ssl
topic: Dynamic media
uuid: 07e2c55b-2388-44c8-83ab-338997c5cb71
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# VideoPlayer.ssl{#videoplayer-ssl}

혼합 미디어 비디오 뷰어에 대한 구성 속성입니다.

>[!NOTE]
>
>이 구성 속성은 기능 팩 NPR-13480이 설치된 [AEM 6.2와](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) 기능 팩 NPR-15011이 설치된 [AEM 6.1에만 적용됩니다](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011).

`[VideoPlayer.|<containerId>_videoPlayer.]ssl=auto|on`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|on</span> </p> </td> 
   <td colname="col2"> <p> 비디오가 보안 SSL 연결(HTTPS) 또는 비보안 연결(HTTP)을 통해 배달되는지 여부를 제어합니다. </p> <p>자동 <span class="codeph"></span> 전송으로 설정하면 비디오 전달 프로토콜이 포함 웹 페이지의 프로토콜에서 상속됩니다. 웹 페이지가 HTTPS를 통해 로드되면 비디오가 HTTPS를 통해 전달되고 그 반대의 경우도 마찬가지입니다. 웹 페이지가 HTTP를 사용하는 경우 비디오가 HTTP를 통해 제공됩니다. </p> <p>켜짐으로 <span class="codeph"> 설정하면</span>웹 페이지 프로토콜에 관계없이 항상 보안 연결을 통해 비디오 배달이 발생합니다. </p> <p>게시된 비디오 전달에만 영향을 주고, 작성 모드에서 비디오 미리 보기에 대해서는 무시됩니다. </p> </td> 
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

보안 비디오 [전달을 참조하십시오](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-securevideodelivery.md#concept-4d155111df9f469aa6c6d7b41e959dcb).
