---
title: HTTP 비디오 전달
description: HTTP 비디오 전달
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 33907e22-107b-4345-82bb-cad47cb7a839
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---

# HTTP 비디오 전달{#http-video-delivery}

<!-- >[!NOTE]
>
>Secure Video Delivery only applies to AEM 6.2 with the installation of [Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) and to AEM 6.1 with installation of [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011). -->

뷰어가 이 섹션의 시작 부분에 설명된 구성으로 작동하는 경우 게시된 비디오 전달은 HTTPS(보안) 및 HTTP(비보안) 모드에서 모두 발생할 수 있습니다. 디폴트 구성에서, 비디오 전달 프로토콜은 임베딩 웹 페이지의 전달 프로토콜을 엄격하게 따른다. 그러나 [VideoPlayer.ssl](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-ssl.md#reference-df0a29aa8a584cebaaa1c7bb6fab362e) 구성 특성을 사용하여 웹 페이지를 포함하는 데 사용되는 프로토콜에 관계없이 HTTPS 비디오 전송을 강제할 수 있습니다. (작성자 모드의 비디오 미리 보기는 항상 HTTPS를 통해 안전하게 제공됩니다.)

Adobe Experience Manager에서 사용하는 Dynamic Media 비디오를 게시하는 방법에 따라 `VideoPlayer.ssl` 구성 특성이 다음에 표시된 대로 다르게 적용됩니다.

* URL을 사용하여 Dynamic Media 비디오를 게시하는 경우 `VideoPlayer.ssl`을(를) URL에 추가합니다. 예를 들어 보안 비디오 전달을 강제 적용하려면 다음 뷰어 URL 예제의 끝에 `&VideoPlayer.ssl=on`을(를) 추가합니다.

  ```
  https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/VideoViewer.html?asset=%2Fcontent%2Fdam%2Fmarketing%2Fshoppable-video%2Fadobe-axis-demo%2FAdobe_AXIS_V3_GRADED-HD.mp4&config=/etc/dam/presets/viewer/Video&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&posterimage=/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4&VideoPlayer.ssl=on
  ```

  [웹 응용 프로그램에 URL 연결](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html?lang=en#dynamic)도 참조하세요.

* 포함 코드가 있는 Dynamic Media 비디오를 게시하는 경우 포함 코드 조각의 다른 뷰어 구성 매개 변수 목록에 `VideoPlayer.ssl`을(를) 추가합니다. 예를 들어 HTTPS 비디오 전송을 강제하려면 다음 예제와 같이 `&VideoPlayer.ssl=on`을(를) 추가합니다.

  ```
  <style type="text/css"> 
   #s7video_div.s7videoviewer{ 
     width:100%;  
     height:auto; 
   } 
  </style> 
  <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/VideoViewer.js"></script> 
  <div id="s7video_div"></div> 
  <script type="text/javascript"> 
   var s7videoviewer = new s7viewers.VideoViewer({ 
    "containerId" : "s7video_div", 
    "params" : {  
     "VideoPlayer.ssl" : "on", 
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

  [웹 페이지에 비디오 포함](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html#dynamic)도 참조하세요.
