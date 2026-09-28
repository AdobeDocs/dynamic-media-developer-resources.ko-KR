---
title: SmartCropVideoPlayer.ssl
description: 스마트 자르기 비디오 뷰어에 대한 구성 속성입니다.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 590ef156-0afe-4e65-b84b-b33f7c7d7b02
TQID: 'https://experienceleague.adobe.com/G5khbuFx9C22D60Iy1X3EgfOHsXleGxSWBpBM3kqey4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
  - id: d09181b5-a36a-43de-ba01-36641440bc43
    internal-label: Experience Manager Assets
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
  - id: fe490c45-63fa-5b99-b5b4-d8cfeda8aa7d
    internal-label: SDK/API
  - id: bd0d2470-932c-4269-8eca-6d939b72d9ef
    internal-label: Dynamic Media
  - id: d4b6216b-4a89-4ff0-8ac0-5a699ba23100
    internal-label: Images and videos
subfeature_v2:
  - id: c12bda38-aa1a-4647-b62e-42cd4537dac6
    internal-label: Dynamic Media Classic
  - id: d17d085a-e808-49dd-b9a6-85a996b999bd
    internal-label: Viewers
  - id: a0cde32c-c339-4649-bd06-f1111bc952fc
    internal-label: Smart Crop
  - id: cb04d42d-1b70-43b0-9951-45998eb6e842
    internal-label: Video
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: 0e24e07f8c91d3e7fda5510ed4252f9953e27467
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 2%
---
# SmartCropVideoPlayer.ssl{#smartcropvideoplayer-ssl}

스마트 자르기 비디오 뷰어에 대한 구성 속성입니다.

<!--
 >[!NOTE]
>
>This configuration attribute only applies to AEM 6.2 with installation of [Feature Pack NPR-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) and to AEM 6.1 with installation of [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011).
-->

`[SmartCropVideoPlayer.|<containerId>_videoPlayer.]ssl=auto|on`

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

[보안 비디오 배달](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-securevideodelivery.md#concept-cf9d1346a07d4429b0c6c32c9cac50ff)도 참조하세요.
