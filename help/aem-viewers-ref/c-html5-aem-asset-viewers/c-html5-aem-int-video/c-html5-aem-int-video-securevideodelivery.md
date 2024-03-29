---
title: HTTPS 비디오 게재
description: HTTPS 비디오 게재
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 68d37b5d-5015-4a98-84b8-8911ace327ed
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 0%

---

# HTTPS 비디오 게재{#https-video-delivery}

<!-- >[!NOTE]
>
>Secure Video Delivery only applies to AEM 6.2 with the installation of [Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) and to AEM 6.1 with installation of [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011). -->

뷰어가 이 섹션의 시작 부분에 설명된 구성으로 작동하는 경우 게시된 비디오 전달은 HTTPS(보안) 및 HTTP(비보안) 모드에서 모두 발생할 수 있습니다. 디폴트 구성에서, 비디오 전달 프로토콜은 임베딩 웹 페이지의 전달 프로토콜을 엄격하게 따른다. 그러나 를 사용하여 웹 페이지를 포함하는 데 사용되는 프로토콜에 관계없이 HTTPS 비디오 전송을 강제할 수 있습니다. [VideoPlayer.ssl](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/r-html5-aem-int-video-config-attrib/r-html5-aem-int-video-config-attrib-videoplayer-ssl.md#reference-c28e1b700977493eadab5489458d7771) 구성 속성입니다. (작성자 모드의 비디오 미리 보기는 항상 HTTPS를 통해 안전하게 제공됩니다.)

게시 방법에 따라 [!DNL Dynamic Media] Adobe Experience Manager에서 사용하는 비디오 `VideoPlayer.ssl` 구성 속성은 다음에 설명된 대로 다르게 적용됩니다.

* 을(를) 게시하는 경우 [!DNL Dynamic Media] URL이 있는 비디오에서는 `VideoPlayer.ssl` URL로 복사합니다. 예를 들어 보안 비디오 전달을 강제 적용하려면 다음을 추가합니다 `&VideoPlayer.ssl=on` 다음 뷰어 URL 예제의 끝:

  ```
  https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/InteractiveVideoViewer.html?asset=%2Fcontent%2Fdam%2Fmarketing%2Fshoppable-video%2Fadobe-axis-demo%2FAdobe_AXIS_V3_GRADED-HD.mp4&config=/etc/dam/presets/viewer/Shoppable_Video_light&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&interactivedata=content/dam/_VTT/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4.svideo.vtt&VideoPlayer.contenturl=https://adobedemo62-h.assetsadobe.com/is/content&VideoPlayer.ssl=on
  ```

  참조: [웹 애플리케이션에 URL 연결](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html?lang=en#dynamic)

* 을(를) 게시하는 경우 [!DNL Dynamic Media] 포함 코드가 있는 비디오, 사용자가 추가 `VideoPlayer.ssl` 포함 코드 조각의 다른 뷰어 구성 매개 변수 목록. 예를 들어 HTTPS 비디오 전송을 강제하려면 다음을 추가합니다 `&VideoPlayer.ssl=on` 다음 예제와 같이:

  ```html {.line-numbers}
  <style type="text/css"> 
   #s7interactivevideo_div.s7interactivevideoviewer{ 
     width:100%;  
     height:auto; 
   } 
  </style> 
  <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
  <div id="s7interactivevideo_div"></div> 
  <script type="text/javascript"> 
   var s7interactivevideoviewer = new s7viewers.InteractiveVideoViewer({ 
    "containerId" : "s7interactivevideo_div", 
    "params" : {  
     "VideoPlayer.ssl" : "on", 
     "serverurl" : "https://adobedemo62-h.assetsadobe.com/is/image", 
     "contenturl" : "https://demos-pub.assetsadobe.com/",  
     "config" : "/etc/dam/presets/viewer/Shoppable_Video_light", 
     "config2": "/etc/dam/presets/analytics", 
     "videoserverurl": "https://gateway-na.assetsadobe.com/DMGateway/public/demoCo", 
     "interactivedata": "content/dam/_VTT/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4.svideo.vtt", 
     "VideoPlayer.contenturl": "https://adobedemo62-h.assetsadobe.com/is/content", 
     "asset" : "/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4" } 
   }) 
   /* // Example of interactive video event for quick view. 
     s7interactivevideoviewer.setHandlers({  
     "quickViewActivate": function(inData) { 
       var sku=inData.sku; //SKU for product ID 
      //To pass other parameter from the hotspot, you must add custom parameter during the hotspot setup as parameterName=value 
      loadQuickView(sku); //Replace this call with your quickview plugin 
      //Please refer to your quickviewer plugin for the quickview call 
      },  
  "initComplete":function() {  
      //--- Attach quickview pop-up to viewer container so pop-up works in fullscreen mode --- 
      var popup = document.getElementById('quickview_div'); // get custom quick view container 
      popup.parentNode.removeChild(popup); // remove it from current DOM 
      var sdkContainerId = s7interactivevideoviewer.getComponent("container").getInnerContainerId(); // get viewer container component 
      var inner_container = document.getElementById(sdkContainerId);  
      inner_container.appendChild(popup); //Attach custom quick view container to viewer 
      }  
     }); 
   */ 
   s7interactivevideoviewer.init(); 
  </script>
  ```

  참조: [웹 페이지에 비디오 포함](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html#dynamic).
