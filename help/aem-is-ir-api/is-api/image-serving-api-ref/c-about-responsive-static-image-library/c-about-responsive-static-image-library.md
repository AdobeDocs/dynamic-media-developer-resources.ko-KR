---
description: 응답형 이미지 라이브러리는 Scene7에서 제공되는 이미지 품질을 동적으로 조정하고 응답형 웹 페이지에 임베드하는 JavaScript 모듈입니다. 또한 고밀도 화면을 갖춘 디바이스에서 향상된 이미지 품질을 제공합니다. 또한 이 라이브러리는 스마트 자르기 및 스마트 색상 견본에서 결과를 응답적으로 렌더링할 수 있습니다.
seo-description: 응답형 이미지 라이브러리는 Scene7에서 제공되는 이미지 품질을 동적으로 조정하고 응답형 웹 페이지에 임베드하는 JavaScript 모듈입니다. 또한 고밀도 화면을 갖춘 디바이스에서 향상된 이미지 품질을 제공합니다. 또한 이 라이브러리는 스마트 자르기 및 스마트 색상 견본에서 결과를 응답적으로 렌더링할 수 있습니다.
seo-title: 반응형 이미지 라이브러리 정보
solution: Experience Manager
title: 반응형 이미지 라이브러리 정보
topic: Scene7 Image Serving - Image Rendering API
uuid: 0906a940-59ff-45b0-b509-57bd02f2da57
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 반응형 이미지 라이브러리 정보{#about-responsive-image-library}

응답형 이미지 라이브러리는 Scene7에서 제공되는 이미지 품질을 동적으로 조정하고 응답형 웹 페이지에 임베드하는 JavaScript 모듈입니다. 또한 고밀도 화면을 갖춘 디바이스에서 향상된 이미지 품질을 제공합니다. 또한 이 라이브러리는 스마트 자르기 및 스마트 색상 견본에서 결과를 응답적으로 렌더링할 수 있습니다.

## 데모 URL {#section-4f72c1dc38bf4e03acfa5205733a05a5}

응답형 이미지 라이브러리의 가장 간단한 사용 사례는 이미지 너비에 대한 중단점 값 목록을 정의하는 것입니다. 이 목록은 사용자가 브라우저 창의 크기를 조정하거나 장치의 방향을 변경하여 웹 페이지 레이아웃이 변경되므로 이미지 크기를 조절할 때 적절한 변환이 로드되고 표시되도록 합니다. 라이브러리는 화면의 이미지 크기를 지속적으로 모니터링하며 새 중단점 너비에 도달할 때마다 Scene7에서 새 이미지 변환을 가져옵니다.

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
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-simple.html" scope="external" format="https"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-simple.html </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-simple.htm--> </p> </td> 
   <td colname="col2"> <p>다음은 반응형 이미지가 웹 페이지 너비의 50%를 차지하는 컨테이너 내에 있는 간단한 예입니다. 브라우저 창의 크기가 변경될 때마다 컨테이너 너비가 변경됩니다. 이미지 너비가 구성된 중단점 중 하나에 도달하면 삽화를 위해 200, 400, 600 및 800픽셀로 설정됩니다. 새 변환이 다운로드되고 표시됩니다. 따라서 불필요한 큰 이미지를 로딩하지 않고 네트워크 대역폭을 저장하는 것이 좋습니다. </p> <p>URL을 클릭하여 웹 페이지를 열고 브라우저 창의 크기를 조정하며 네트워크 트래픽을 모니터링합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-bootstrap.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-bootstrap.html </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-bootstrap.htm--> </p> </td> 
   <td colname="col2"> <p>다음 Bootstrap 예는 웹 페이지에서 동일한 사용 사례를 보여줍니다. Bootstrap CSS에 따르면 반응형 이미지가 추가되는 레이아웃 셀은 다음 너비 중 하나를 사용할 수 있습니다.360, 720 및 940픽셀 반응형 이미지 라이브러리에 중단점으로 전달되는 정확한 값입니다. 따라서 Scene7에서는 클라이언트의 네트워크 대역폭이 효과적으로 사용되도록 합니다. 또한 클라이언트측 브라우저의 크기를 조정하더라도 시각적 결함이 없이 현재 웹 페이지 레이아웃에 필요한 정확한 크기로 이미지가 표시되도록 합니다. </p> <p>URL을 클릭하여 웹 페이지를 열고 브라우저 창의 크기를 조정하여 다양한 레이아웃 중단점에 맞추고 네트워크 트래픽을 모니터링합니다. </p> <p>더 많은 고급 사용 사례로는 다른 이미지 사전 설정 또는 이미지 제공 명령 또는 둘 다를 다른 중단점 값에 연결하는 것이 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/image-presets.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/image-presets.html </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/image-presets.html--> </p> </td> 
   <td colname="col2"> <p>다음 예제에서는 다양한 중단점 크기에 대해 서로 다른 이미지 품질과 형식의 이미지 사전 설정이 사용됩니다. 작은 중단점의 경우 이미지 제공에서 6가지 색상으로만 압축된 GIF 이미지를 반환하도록 하는 저품질의 사전 설정이 적용됩니다. 중간 중단점이 고압축 JPEG용으로 구성된 이미지 사전 설정을 사용하고 있습니다. 가장 큰 중단점은 손실 없는 PNG를 사용하여 고품질 이미지 사전 설정과 연결됩니다. 이러한 방법을 사용하면 큰 화면을 가진 장치의 대역폭 및 처리 능력이 높다는 가정 하에 고품질의 이미지가 이러한 디바이스에 전달되도록 할 수 있습니다. </p> <p>URL을 클릭하여 웹 페이지를 열고 웹 브라우저 창의 크기를 확대에서 더 작게 조정하여 이미지 품질이 어떻게 저하되는지 확인합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/crops.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/crops.html </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/crops.html--> </p> </td> 
   <td colname="col2"> <p>이미지 사전 설정 외에도 특정 이미지 제공 명령을 중단점과 연결할 수 있습니다. 다음 예에서는 화면의 이미지 크기가 작아지면서 배너 이미지를 관심 영역으로 점차적으로 자르는 방법을 보여줍니다. 여기서는 가장 큰 중단점에 이미지 제공 명령이 전혀 없으므로 배너 이미지가 완전히 표시됩니다. 중간 중단점에서 중간 자르기가 적용되어 텍스트 "실행 중"이 있는 주자만 표시됩니다. 작은 중단점에서는 제품만 표시되도록 더 많은 자르기가 적용됩니다. </p> <p>URL을 클릭하여 웹 페이지를 열고 브라우저 창의 크기를 조정합니다. 큰 이미지에서 작은 크기로 갈수록 이미지가 점점 잘립니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/template.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/template.html </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/template.html--> </p> </td> 
   <td colname="col2"> <p>이미지 제공 템플릿과 함께 이미지 제공 명령을 사용하여 이미지 크기를 기반으로 특정 템플릿 매개 변수를 제어할 수도 있습니다. 다음 예에서는 <span class="codeph"> $fontsize </span> 매개 변수를 사용하여 텍스트 오버레이의 글꼴 크기를 매개 변수화하는 이미지 제공 템플릿을 사용합니다. 응답 속도가 빠른 이미지는 더 작은 이미지 크기에 대해 더 큰 글꼴 크기를 사용하여 텍스트를 항상 읽을 수 있도록 구성됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 시스템 요구 사항 {#section-35ea9e9c79cc43d7bcefdc240340fba4}

**서버 하드웨어 및 소프트웨어**

* Scene7 Image Serving 6.0.1 이상.

**클라이언트 브라우저 최소 요구 사항**

* Microsoft® Windows® 7 이상Mac OS X 10.8 이상
* Firefox 23, Safari 6, Chrome 29, IE 9 이상.
* iOS 6 이상.
* iPhone3GS 이상 및 iPad2 이상에서 인증(기본 브라우저만 해당)
* Android OS 2.3 이상.
* 지금은 모바일 장치의 Internet Explorer가 지원되지 않습니다.

