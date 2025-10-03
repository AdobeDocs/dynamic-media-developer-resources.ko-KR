---
description: 반응형 이미지 라이브러리 는 Dynamic Media에서 제공되고 반응형 웹 페이지에 임베드된 이미지의 품질을 동적으로 조정하는 JavaScript 모듈입니다. 또한 고밀도 스크린을 사용하는 장치에서 향상된 이미지 품질을 제공합니다. 또한 라이브러리는 스마트 자르기 및 스마트 색상 견본의 결과를 응답형으로 렌더링할 수 있습니다.
solution: Experience Manager
title: 응답형 이미지 라이브러리 정보
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f853b9b4-917c-4744-b2a5-25fde2532356
source-git-commit: ce1ac4938c7baf482c6c55a9ad13379153a3ec5b
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---

# 응답형 이미지 라이브러리 정보{#about-responsive-image-library}

반응형 이미지 라이브러리 는 Dynamic Media에서 제공되고 반응형 웹 페이지에 임베드된 이미지의 품질을 동적으로 조정하는 JavaScript 모듈입니다. 또한 고밀도 스크린을 사용하는 장치에서 향상된 이미지 품질을 제공합니다. 또한 라이브러리는 스마트 자르기 및 스마트 색상 견본의 결과를 응답형으로 렌더링할 수 있습니다.

## 데모 URL {#section-4f72c1dc38bf4e03acfa5205733a05a5}

응답형 이미지 라이브러리의 가장 간단한 사용 사례는 이미지 너비에 대한 중단점 값 목록을 정의하는 것입니다. 이 목록은 사용자가 브라우저 창의 크기를 조정하거나 장치의 방향을 변경하면 웹 페이지 레이아웃이 변경되어 이미지 크기가 조정될 때 적절한 렌디션이 로드되고 표시되도록 합니다. 라이브러리는 화면 이미지 크기를 지속적으로 모니터링하며 새 중단점 너비에 도달할 때마다 Dynamic Media에서 새 이미지 렌디션을 가져옵니다.

<!--

<table id="table_3D3D3991B802461A888E1093C1217D26"> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Demo URL </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-simple.html" scope="external" format="https"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-simple.html </a> </p></td> 
   <td colname="col2"> <p>The following is a simple example where the responsive image is within a container that takes 50% of the web page width. Every time the browser window is resized the container width changes. When the image width reaches one of the configured breakpoints-which are set at 200, 400, 600 and 800 pixels for illustrative purposes-a new rendition is downloaded and displayed. The goal is to avoid loading unnecessary large images and save network bandwidth. </p> <p>Click the URL so you open the web page, resize the browser window, and monitor network traffic. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-bootstrap.html" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-bootstrap.html </a> </p></td> 
   <td colname="col2"> <p>The following Bootstrap example illustrates the same use case in a web page. According to Bootstrap CSS, the layout cell to which the responsive image is added can take one of the following widths: 360, 720 and 940 pixels. These values are exactly what is passed as breakpoints to the Responsive Image Library. As such, Dynamic Media ensures that the client's network bandwidth is used effectively. And, it also ensures that the image is displayed in the exact size needed-given the current web page layout-without any visual artifacts from scaling the client-side browser. </p> <p>Click the URL so you open the web page, resize the browser window to hit different layout breakpoints, and monitor network traffic. </p> <p>More advanced use cases include associating different Image Presets, or Image Serving commands, or both, with different breakpoint values. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/image-presets.html" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/image-presets.html</a> </p></td> 
   <td colname="col2"> <p>In this next example, Image Presets of different image quality and format for different breakpoint sizes are used. For a small breakpoint, a low-quality preset is applied which forces Image Serving to return the GIF image compressed to six colors only. A medium breakpoint is using an Image Preset configured for JPEG with high compression. The largest breakpoint is associated with a high-quality Image Preset using lossless PNG. Such method ensures that high-quality images are delivered to such devices, based on the assumption that devices with larger screens have greater bandwidth and processing power. </p> <p>Click the URL so you open the web page, resize the web browser window from larger to smaller and notice how the image quality degrades. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/crops.html" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/crops.html </a> </p></td> 
   <td colname="col2"> <p>In addition to Image Presets, it is possible to associate specific Image Serving commands with breakpoints. The following example shows how it is possible to gradually crop the banner image to the region of interest as the onscreen image size becomes smaller. Here, the largest breakpoint does not have any Image Serving commands at all, so the banner image is fully visible. At medium breakpoint applies moderate cropping, making only the runner with text "Running" visible. At small breakpoint, more cropping is applied so that only the product is shown. </p> <p>Click the URL so you open the web page and resize your browser window. Notice how the image crops gradually as you go from a larger to a smaller size. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/template.html" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/template.html </a> </p></td> 
   <td colname="col2"> <p>You can also use Image Serving commands with Image Serving Templates to control certain template parameters based on the image size. In this next example, an Image Serving Template is used where the font size of the text overlay is parameterized using <span class="codeph"> $fontsize </span> parameter. Responsive image is configured to use a larger font size for smaller image sizes to ensure that text always remains readable: </p> </td> 
  </tr> 
 </tbody> 
</table>

-->

## 시스템 요구 사항 {#section-35ea9e9c79cc43d7bcefdc240340fba4}

**서버 하드웨어 및 소프트웨어**

* Dynamic Media 이미지 제공 6.0.1 이상.

**클라이언트 브라우저 최소 요구 사항**

* Microsoft® Windows® 7 이상, macOS X 10.8 이상
* Firefox 23, Safari 6, Chrome 29, IE 9 이상
* iOS 6 이상
* iPhone3GS 이상 및 iPad2 이상에서 인증됨(기본 브라우저만 해당).
* Android™ OS 2.3 이상
* 모바일 장치의 Internet Explorer는 현재 지원되지 않습니다.
