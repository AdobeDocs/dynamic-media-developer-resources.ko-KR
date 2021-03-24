---
description: HTTPS 비디오 전달
solution: Experience Manager
title: HTTPS 비디오 전달
feature: Dynamic Media Classic,뷰어,SDK/API,혼합 미디어 집합
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---


# HTTPS 비디오 배달{#https-video-delivery}

>[!NOTE]
>
>보안 비디오 배달은 [기능 팩-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480)이 설치된 AEM 6.2와 [기능 팩 NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011)이 설치된 AEM 6.1에만 적용됩니다.

뷰어가 이 섹션의 시작 부분에서 설명한 대로 구성에서 작동한다면 게시된 비디오 배달은 HTTPS(보안) 및 HTTP(비보안) 모드에서 모두 발생할 수 있습니다. 기본 구성에서 비디오 전달 프로토콜은 포함 웹 페이지의 배달 프로토콜을 엄격하게 따릅니다. 그러나 [VideoPlayer.ssl](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-ssl.md#reference-df0a29aa8a584cebaaa1c7bb6fab362e) 구성 특성을 사용하여 웹 페이지를 임베드하는 데 사용되는 프로토콜에 관계없이 HTTPS 비디오를 강제 제공할 수 있습니다. (작성자 모드에서 비디오 미리 보기는 항상 HTTPS를 통해 안전하게 제공됩니다.)

AEM에서 사용하는 Dynamic Media 비디오를 게시하는 방법에 따라 `VideoPlayer.ssl` 구성 속성이 다음에 설명된 대로 다르게 적용됩니다.

* URL이 있는 Dynamic Media 비디오를 게시하면 URL에 `VideoPlayer.ssl`을 추가합니다. 예를 들어 보안 비디오 제공을 강제 수행하려면 다음 뷰어 URL 예제의 끝에 `&VideoPlayer.ssl=on`을 추가합니다.

   ```
   https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/MixedMediaViewer.html?asset=%2Fcontent%2Fdam%2FGeometrixx-Outdoors-New-Launch%2Fbackpack%2Fbackpack_mixed_media&config=/etc/dam/presets/viewer/MixedMedia_light&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&VideoPlayer.ssl=on
   ```

   [(URL을 웹 응용 프로그램에 연결](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html?lang=en#dynamic)을 참조하십시오.

* 포함 코드를 사용하여 Dynamic Media 비디오를 게시하면 포함 코드 조각에 있는 다른 뷰어 구성 매개 변수 목록에 `VideoPlayer.ssl`을 추가합니다. 예를 들어 HTTPS 비디오 제공을 강제 수행하려면 다음 예제와 같이 `&VideoPlayer.ssl=on`을 추가합니다.

   ```
   <style type="text/css"> 
    #s7mixedmedia_div.s7mixedmediaviewer{ 
      width:100%;  
      height:auto; 
    } 
   </style> 
   <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/MixedMediaViewer.js"></script> 
   <div id="s7mixedmedia_div"></div> 
   <script type="text/javascript"> 
    var s7mixedmediaviewer = new s7viewers.MixedMediaViewer({ 
     "containerId" : "s7mixedmedia_div", 
     "params" : {  
      "VideoPlayer.ssl" : "on", 
      "serverurl" : "https://adobedemo62-h.assetsadobe.com/is/image", 
      "contenturl" : "https://demos-pub.assetsadobe.com/",  
      "config" : "/etc/dam/presets/viewer/MixedMedia_light", 
      "config2": "/etc/dam/presets/analytics", 
      "videoserverurl": "https://gateway-na.assetsadobe.com/DMGateway/public/demoCo", 
      "asset" : "/content/dam/Geometrixx-Outdoors-New-Launch/backpack/backpack_mixed_media" } 
    }).init(); 
   </script>
   ```

   [(웹 페이지에 비디오 포함](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html#dynamic) 참조

