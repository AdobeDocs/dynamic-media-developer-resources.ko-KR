---
description: 널
seo-description: 널
seo-title: HTTPS 비디오 전달
solution: Experience Manager
title: HTTPS 비디오 전달
topic: Dynamic media
uuid: acda9c8f-e8f4-4855-9b14-82838ec5a1b9
translation-type: tm+mt
source-git-commit: 6cff4553307fe6cbda4b80ce3f39b58e615fa365

---


# HTTPS 비디오 전달{#https-video-delivery}

>[!NOTE]
>
>보안 비디오 게시는 기능 팩-13480이 설치된 AEM 6.2 [와](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) 기능 팩 NPR-15011 [이 설치된 AEM 6.1에만 적용됩니다](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011).

뷰어가 이 섹션의 시작 부분에서 설명한 대로 구성에서 작동하면 게시된 비디오 배달은 HTTPS(보안) 및 HTTP(비보안) 모드에서 모두 발생할 수 있습니다. 기본 구성에서는 비디오 배달 프로토콜이 내장 웹 페이지의 배달 프로토콜을 엄격하게 따릅니다. 그러나 VideoPlayer.ssl 구성 특성을 사용하여 웹 페이지를 임베드하는 데 사용되는 프로토콜에 상관 없이 HTTPS [비디오를](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/r-html5-aem-int-video-config-attrib/r-html5-aem-int-video-config-attrib-videoplayer-ssl.md#reference-c28e1b700977493eadab5489458d7771) 강제로 제공할 수 있습니다. (작성자 모드에서 비디오 미리 보기는 항상 HTTPS를 통해 안전하게 제공됩니다.)

AEM에서 사용하는 Dynamic Media 비디오를 게시하는 방법에 따라 `VideoPlayer.ssl` 구성 속성이 다음과 같이 다르게 적용됩니다.

* URL을 사용하여 Dynamic Media 비디오를 게시하면 URL에 `VideoPlayer.ssl` 추가됩니다. 예를 들어 보안 비디오 제공을 강제 적용하려면 다음 뷰어 URL 예제의 `&VideoPlayer.ssl=on` 끝에 추가합니다.

   ```
   https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/InteractiveVideoViewer.html?asset=%2Fcontent%2Fdam%2Fmarketing%2Fshoppable-video%2Fadobe-axis-demo%2FAdobe_AXIS_V3_GRADED-HD.mp4&config=/etc/dam/presets/viewer/Shoppable_Video_light&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&interactivedata=content/dam/_VTT/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4.svideo.vtt&VideoPlayer.contenturl=https://adobedemo62-h.assetsadobe.com/is/content&VideoPlayer.ssl=on
   ```

   See also [Linking URLs to your Web Application](https://docs.adobe.com/content/help/en/experience-manager-64/assets/dynamic/linking-urls-to-yourwebapplication.html)

* 포함 코드를 사용하여 Dynamic Media 비디오를 게시하면 포함 코드 조각에 있는 다른 뷰어 구성 매개 변수 `VideoPlayer.ssl` 목록에 추가됩니다. 예를 들어 HTTPS 비디오 제공을 강제 적용하려면 다음 예와 `&VideoPlayer.ssl=on` 같이 추가합니다.

   ```
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
       //To pass other parameter from the hotspot, you will need to add custom parameter during the hotspot setup as parameterName=value 
       loadQuickView(sku); //Replace this call with your quickview plugin 
       //Please refer to your quickviewer plugin for the quickview call 
       },  
   "initComplete":function() {  
       //--- Attach quickview popup to viewer container so popup will work in fullscreen mode --- 
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

   See also [Embedding the Video on a Web Page](https://docs.adobe.com/content/help/en/experience-manager-64/assets/dynamic/linking-urls-to-yourwebapplication.html).

