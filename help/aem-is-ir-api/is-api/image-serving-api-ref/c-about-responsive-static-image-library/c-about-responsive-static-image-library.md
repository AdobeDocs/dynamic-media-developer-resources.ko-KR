---
description: 응답형 이미지 라이브러리는 Dynamic Media에서 제공되는 이미지의 품질을 동적으로 조정하고 응답형 웹 페이지에 포함된 JavaScript 모듈입니다. 또한, 고밀도 화면을 사용하는 장치의 이미지 품질을 향상시킬 수 있습니다. 또한 라이브러리가 [스마트 자르기] 및 [스마트 견본]의 결과를 응답적으로 렌더링할 수도 있습니다.
solution: Experience Manager
title: 응답형 이미지 라이브러리 정보
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: f853b9b4-917c-4744-b2a5-25fde2532356
source-git-commit: 417fd2540c15762356dfb60aa7eb635ee5f74d13
workflow-type: tm+mt
source-wordcount: '922'
ht-degree: 0%

---

# 응답형 이미지 라이브러리 정보{#about-responsive-image-library}

응답형 이미지 라이브러리는 Dynamic Media에서 제공되는 이미지의 품질을 동적으로 조정하고 응답형 웹 페이지에 포함된 JavaScript 모듈입니다. 또한, 고밀도 화면을 사용하는 장치의 이미지 품질을 향상시킬 수 있습니다. 또한 라이브러리가 [스마트 자르기] 및 [스마트 견본]의 결과를 응답적으로 렌더링할 수도 있습니다.

## 데모 URL {#section-4f72c1dc38bf4e03acfa5205733a05a5}

응답형 이미지 라이브러리의 가장 간단한 사용 사례는 이미지 너비에 대한 중단점 값 목록을 정의하는 것입니다. 이 목록에서는 브라우저 창의 크기를 조정하거나 장치의 방향을 변경하는 사용자의 웹 페이지 레이아웃으로 인해 이미지 크기가 변경될 때 적절한 표현식이 로드되고 표시됩니다. 라이브러리는 계속해서 온스크린 이미지 크기를 모니터링하고 새 중단점 너비에 도달할 때마다 Dynamic Media의 새 이미지 표현물을 가져옵니다.

<table id="table_3D3D3991B802461A888E1093C1217D26"> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>데모 URL </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-simple.html" scope="external" format="https"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-simple.html  </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-simple.htm--> </p> </td> 
   <td colname="col2"> <p>다음은 응답형 이미지가 웹 페이지 너비의 50%를 차지하는 컨테이너 내에 있는 간단한 예입니다. 브라우저 창의 크기가 변경될 때마다 컨테이너 너비가 변경됩니다. 이미지 너비가 삽화를 위해 200, 400, 600 및 800픽셀로 설정된 구성된 중단점 중 하나에 도달하면 새 표현물이 다운로드되어 표시됩니다. 불필요한 큰 이미지를 로드하지 않고 네트워크 대역폭을 절약하는 것이 목표입니다. </p> <p>웹 페이지를 열고 브라우저 창의 크기를 조정하고 네트워크 트래픽을 모니터링하려면 URL을 클릭합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-bootstrap.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-bootstrap.html  </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-bootstrap.htm--> </p> </td> 
   <td colname="col2"> <p>다음 Bootstrap 예는 웹 페이지에서도 동일한 사용 사례를 보여줍니다. Bootstrap CSS에 따라 응답형 이미지가 추가된 레이아웃 셀은 다음 너비 중 하나를 사용할 수 있습니다.360, 720 및 940픽셀 이러한 값은 응답형 이미지 라이브러리에 중단점으로 전달되는 것과 같습니다. 따라서 Dynamic Media에서는 클라이언트의 네트워크 대역폭을 효과적으로 사용할 수 있습니다. 또한 클라이언트 측 브라우저 크기 조절의 시각적 아티팩트가 없이 현재 웹 페이지 레이아웃에 필요한 정확한 크기로 이미지가 표시되도록 합니다. </p> <p>웹 페이지를 열고, 브라우저 창의 크기를 조정하여 다른 레이아웃 중단점을 맞추고, 네트워크 트래픽을 모니터링하도록 URL을 클릭합니다. </p> <p>더 고급 사용 사례에는 서로 다른 이미지 사전 설정 또는 이미지 제공 명령 또는 둘 다 다른 중단점 값과 연결하는 작업이 포함됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/image-presets.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/image-presets.html  </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/image-presets.html--> </p> </td> 
   <td colname="col2"> <p>다음 예에서는 다양한 중단점 크기에 대해 서로 다른 이미지 품질 및 형식의 이미지 사전 설정이 사용됩니다. 작은 중단점의 경우, 이미지 제공 기능이 6색으로 압축된 GIF 이미지를 반환하도록 하는 낮은 품질 사전 설정이 적용됩니다. 미디어 중단점이 압축률이 높은 JPEG용으로 구성된 이미지 사전 설정을 사용하고 있습니다. 가장 큰 중단점은 손실 없는 PNG를 사용하여 고품질 이미지 사전 설정과 연결됩니다. 이러한 방법은 큰 화면을 가진 장치가 더 큰 대역폭과 처리 능력을 가지고 있다는 가정을 기반으로, 이러한 장치에 고품질 이미지가 전달되도록 합니다. </p> <p>웹 페이지를 열고, 웹 브라우저 창의 크기를 더 큰 창에서 더 작은 크기로 조정하고, 이미지 품질이 어떻게 저하되는지 확인합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/crops.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/crops.html  </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/crops.html--> </p> </td> 
   <td colname="col2"> <p>이미지 사전 설정 외에도 특정 이미지 제공 명령을 중단점과 연결할 수 있습니다. 다음 예제에서는 스크린의 이미지 크기가 작아지면서 배너 이미지를 관심 영역으로 점진적으로 자르는 방법을 보여줍니다. 여기서는 가장 큰 중단점에 이미지 제공 명령이 전혀 없으므로 배너 이미지가 완전히 표시됩니다. 중간 중단점에서 중간 자르기가 적용되어 "실행 중"이라는 텍스트가 있는 러너만 표시됩니다. 작은 중단점에서는 제품만 표시되도록 더 많은 자르기가 적용됩니다. </p> <p>웹 페이지를 열고 브라우저 창의 크기를 조정하도록 URL을 클릭합니다. 크기가 더 큰 것부터 작은 크기로 갈수록 이미지가 어떻게 자르는지 확인하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/template.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/template.html  </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/template.html--> </p> </td> 
   <td colname="col2"> <p>또한 이미지 제공 템플릿 과 함께 이미지 제공 명령을 사용하여 이미지 크기에 따라 특정 템플릿 매개 변수를 제어할 수도 있습니다. 다음 예에서는 텍스트 오버레이의 글꼴 크기가 <span class="codeph"> $fontsize </span> 매개 변수를 사용하여 매개 변수화되는 이미지 제공 템플릿이 사용됩니다. 응답형 이미지는 더 작은 이미지 크기에 대해 더 큰 글꼴 크기를 사용하여 텍스트를 항상 읽을 수 있도록 구성됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 시스템 요구 사항 {#section-35ea9e9c79cc43d7bcefdc240340fba4}

**서버 하드웨어 및 소프트웨어**

* Dynamic Media Image Serving 6.0.1 이상

**클라이언트 브라우저 최소 요구 사항**

* Microsoft® Windows® 7 이상macOS X 10.8 이상
* Firefox 23, Safari 6, Chrome 29, IE 9 이상.
* iOS 6 이상.
* iPhone3GS 이상 및 iPad2 이상에서 인증(기본 브라우저만 해당).
* Android™ OS 2.3 이상.
* 모바일 장치의 Internet Explorer는 현재 지원되지 않습니다.
