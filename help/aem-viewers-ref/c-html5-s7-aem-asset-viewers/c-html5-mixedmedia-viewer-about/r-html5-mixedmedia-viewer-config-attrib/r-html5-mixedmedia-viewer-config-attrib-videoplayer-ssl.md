---
title: VideoPlayer.ssl
description: 혼합 미디어 비디오 뷰어에 대한 구성 속성입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 5fd3aa39-edb0-4434-aa5f-e511c84cf950
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 2%

---

# VideoPlayer.ssl{#videoplayer-ssl}

혼합 미디어 비디오 뷰어에 대한 구성 속성입니다.

<!-- >[!NOTE]
>
>This configuration attribute only applies to AEM 6.2 with installation of [Feature Pack NPR-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) and to AEM 6.1 with installation of [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011). -->

`[VideoPlayer.|<containerId>_videoPlayer.]ssl=auto|on`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 자동|켜기</span> </p> </td> 
   <td colname="col2"> <p> 비디오가 보안 SSL 연결(HTTPS) 또는 비보안 연결(HTTP)을 통해 전달되는지 여부를 제어합니다. </p> <p><span class="codeph"> auto</span>(으)로 설정된 경우 비디오 게재 프로토콜은 포함된 웹 페이지의 프로토콜에서 상속됩니다. 웹 페이지가 HTTPS를 통해 로드되면 비디오도 HTTPS를 통해 전달되며 반대로 전달됩니다. 웹 페이지가 HTTP를 사용하는 경우 비디오는 HTTP를 통해 전달됩니다. </p> <p></span>에 <span class="codeph">(으)로 설정된 경우 비디오 게재는 웹 페이지 프로토콜에 관계없이 항상 보안 연결을 통해 발생합니다. </p> <p>게시된 비디오 게재에만 영향을 미치며 작성자 모드의 비디오 미리 보기에는 무시됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-f42369774e2740dcb399626a0e4e930e}

선택적.

## 기본값 {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## 예 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
ssl=on
```

<!--<a id="section_5943AC73316749C68761FF7F74DA7547"></a>-->

[보안 비디오 배달](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-securevideodelivery.md#concept-4d155111df9f469aa6c6d7b41e959dcb)도 참조하세요.
