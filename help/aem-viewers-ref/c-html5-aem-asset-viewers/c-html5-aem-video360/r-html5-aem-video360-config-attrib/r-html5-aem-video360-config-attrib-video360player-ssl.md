---
description: Video360 뷰어에 대한 구성 속성입니다.
seo-description: Video360 뷰어에 대한 구성 속성입니다.
seo-title: Video360Player.ssl
solution: Experience Manager
title: Video360Player.ssl
topic: Dynamic media
uuid: 00c8295c-cc41-489c-a444-ba9189426a20
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 5%

---


# Video360Player.ssl{#video-player-ssl}

Video360 뷰어에 대한 구성 속성입니다.

>[!NOTE]
>
>이 구성 속성은 [Feature Pack NPR-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480)이 설치된 AEM 6.2와 [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011)이 설치된 AEM 6.1에만 적용됩니다.

`[Video360Player.|<containerId>_video360Player.]ssl=auto|on`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 자동|설정</span> </p> </td> 
   <td colname="col2"> <p> 비디오가 보안 SSL 연결(HTTPS) 또는 비보안 연결(HTTP)을 통해 제공되는지 여부를 제어합니다. </p> <p><span class="codeph"> auto</span>로 설정하면 비디오 전달 프로토콜이 포함 웹 페이지의 프로토콜에서 상속됩니다. 웹 페이지가 HTTPS를 통해 로드되는 경우 비디오는 HTTPS를 통해 전달되거나 그 반대의 경우도 마찬가지입니다. 웹 페이지가 HTTP를 사용하는 경우 비디오는 HTTP를 통해 전달됩니다. </p> <p></span>에서 <span class="codeph">으로 설정하면 웹 페이지 프로토콜에 관계없이 항상 보안 연결을 통해 비디오 배달이 발생합니다. </span></p> <p>게시된 비디오 전달에만 영향을 주고 [작성자] 모드에서 비디오 미리 보기에 대해 무시됩니다. </p> </td> 
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

[보안 비디오 배달](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-securevideodelivery.md#concept-13f66fdd4a52494aa516cd0f36fdac27)도 참조하십시오.
