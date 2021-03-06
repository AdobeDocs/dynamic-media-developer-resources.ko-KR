---
title: HTTP 비디오 게재
description: HTTP 비디오 게재
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 0%

---

# HTTP 비디오 게재{#http-video-delivery}

<!-- >[!NOTE]
>
>Secure Video Delivery only applies to AEM 6.2 with the installation of [Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) and to AEM 6.1 with installation of [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011). -->

뷰어가 이 섹션의 시작 부분에 요약된 대로 구성에서 작동하는 경우 게시된 비디오 배달이 HTTPS(보안) 및 HTTP(비보안) 모드에서 모두 발생할 수 있습니다. 기본 구성에서는 비디오 게재 프로토콜이 포함 웹 페이지의 게재 프로토콜을 엄격히 따릅니다. 그러나 를 사용하여 웹 페이지를 포함하여 사용하는 프로토콜에 관계없이 HTTPS 비디오 제공을 강제 적용할 수 있습니다 [SmartCropVideoPlayer.ssl](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-ssl.md#reference-df0a29aa8a584cebaaa1c7bb6fab362e) 구성 속성입니다. (작성자 모드의 비디오 미리 보기는 항상 HTTPS에서 안전하게 전달됩니다.)

Adobe Experience Manager에서 사용하는 Dynamic Media 비디오를 게시하는 방법에 따라 `SmartCropVideoPlayer.ssl` 구성 속성은 다음과 같이 다르게 적용됩니다.

* URL이 있는 Dynamic Media 비디오를 게시하면 사용자가 추가합니다 `SmartCropVideoPlayer.ssl` 아래와 같이 변경하는 것을 의미합니다. 예를 들어 보안 비디오 제공을 강제 수행하려면 을 추가합니다 `&SmartCropVideoPlayer.ssl=on` 다음 뷰어 URL 예제의 끝:

   ```
   https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/SmartCropVideoViewer.html?asset=%2Fcontent%2Fdam%2Fmarketing%2Fshoppable-video%2Fadobe-axis-demo%2FAdobe_AXIS_V3_GRADED-HD.mp4&config=/etc/dam/presets/viewer/Video&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&posterimage=/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4&SmartCropVideoPlayer.ssl=on
   ```

   참조 - [URL을 웹 애플리케이션에 연결](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html?lang=en#dynamic).

* 포함 코드가 있는 Dynamic Media 비디오를 게시하면 다음을 추가합니다 `SmartCropVideoPlayer.ssl` 포함 코드 조각에 있는 다른 뷰어 구성 매개 변수 목록에 추가합니다. 예를 들어 HTTPS 비디오 제공을 강제 수행하려면 다음을 추가합니다 `&SmartCropVideoPlayer.ssl=on` 다음 예와 같습니다.

   ```
   <style type="text/css"> 
    #s7video_div.s7videoviewer{ 
      width:100%;  
      height:auto; 
    } 
   </style> 
   <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
   <div id="s7video_div"></div> 
   <script type="text/javascript"> 
    var s7videoviewer = new s7viewers.SmartCropVideoViewer({ 
     "containerId" : "s7video_div", 
     "params" : {  
      "SmartCropVideoPlayer.ssl" : "on", 
      "serverurl" : "https://adobedemo62-h.assetsadobe.com/is/image", 
      "contenturl" : "https://demos-pub.assetsadobe.com/",  
      "config" : "/etc/dam/presets/viewer/Video", 
      "config2": "/etc/dam/presets/analytics", 
      "videoserverurl": "https://gateway-na.assetsadobe.com/DMGateway/public/demoCo", 
      "posterimage": "/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4", 
      "asset" : "/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4" } 
    }).init(); 
   </script>
   ```

   참조 - [웹 페이지에 비디오 포함](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html#dynamic).
