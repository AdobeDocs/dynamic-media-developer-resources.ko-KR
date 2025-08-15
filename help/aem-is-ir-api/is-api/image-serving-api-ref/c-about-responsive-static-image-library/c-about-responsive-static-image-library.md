---
description: 반응형 이미지 라이브러리 는 Dynamic Media에서 제공되고 반응형 웹 페이지에 임베드된 이미지의 품질을 동적으로 조정하는 JavaScript 모듈입니다. 또한 고밀도 스크린을 사용하는 장치에서 향상된 이미지 품질을 제공합니다. 또한 라이브러리는 스마트 자르기 및 스마트 색상 견본의 결과를 응답형으로 렌더링할 수 있습니다.
solution: Experience Manager
title: 응답형 이미지 라이브러리 정보
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f853b9b4-917c-4744-b2a5-25fde2532356
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '804'
ht-degree: 0%

---

# 응답형 이미지 라이브러리 정보{#about-responsive-image-library}

반응형 이미지 라이브러리 는 Dynamic Media에서 제공되고 반응형 웹 페이지에 임베드된 이미지의 품질을 동적으로 조정하는 JavaScript 모듈입니다. 또한 고밀도 스크린을 사용하는 장치에서 향상된 이미지 품질을 제공합니다. 또한 라이브러리는 스마트 자르기 및 스마트 색상 견본의 결과를 응답형으로 렌더링할 수 있습니다.

## 데모 URL {#section-4f72c1dc38bf4e03acfa5205733a05a5}

응답형 이미지 라이브러리의 가장 간단한 사용 사례는 이미지 너비에 대한 중단점 값 목록을 정의하는 것입니다. 이 목록은 사용자가 브라우저 창의 크기를 조정하거나 장치의 방향을 변경하면 웹 페이지 레이아웃이 변경되어 이미지 크기가 조정될 때 적절한 렌디션이 로드되고 표시되도록 합니다. 라이브러리는 화면 이미지 크기를 지속적으로 모니터링하며 새 중단점 너비에 도달할 때마다 Dynamic Media에서 새 이미지 렌디션을 가져옵니다.

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
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-simple.html?lang=ko" scope="external" format="https"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-simple.html?lang=ko </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-simple.htm--> </p> </td> 
   <td colname="col2"> <p>다음은 응답형 이미지가 웹 페이지 너비의 50%를 차지하는 컨테이너 내에 있는 간단한 예입니다. 브라우저 창의 크기가 변경될 때마다 컨테이너 너비가 변경됩니다. 이미지 너비가 200, 400, 600 및 800픽셀로 설정된 구성된 중단점 중 하나에 도달하면 새로운 렌디션이 다운로드되어 표시됩니다. 목표는 불필요한 대용량 이미지 로드를 피하고 네트워크 대역폭을 절약하는 것입니다. </p> <p>URL을 클릭하여 웹 페이지를 열고 브라우저 창의 크기를 조정하고 네트워크 트래픽을 모니터링합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-bootstrap.html?lang=ko" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-bootstrap.html?lang=ko </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-bootstrap.htm--> </p> </td> 
   <td colname="col2"> <p>다음 Bootstrap 예제는 웹 페이지의 동일한 사용 사례를 보여 줍니다. Bootstrap CSS에 따르면 응답형 이미지가 추가된 레이아웃 셀은 360, 720 및 940 픽셀 너비 중 하나를 사용할 수 있습니다. 이러한 값은 응답형 이미지 라이브러리에 중단점으로 전달되는 것입니다. 따라서 Dynamic Media는 클라이언트의 네트워크 대역폭이 효과적으로 사용되도록 합니다. 또한 클라이언트측 브라우저의 크기 조절로 인한 시각적 아티팩트 없이 이미지가 현재 웹 페이지 레이아웃에 따라 필요한 정확한 크기로 표시되도록 합니다. </p> <p>URL을 클릭하여 웹 페이지를 열고 브라우저 창의 크기를 변경하여 다른 레이아웃 중단점을 히트하고 네트워크 트래픽을 모니터링합니다. </p> <p>고급 사용 사례에는 서로 다른 이미지 사전 설정이나 이미지 제공 명령 또는 둘 다를 다른 중단점 값과 연결하는 것이 포함됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/image-presets.html?lang=ko" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/image-presets.html?lang=ko</a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/image-presets.html--> </p> </td> 
   <td colname="col2"> <p>다음 예제에서는 서로 다른 중단점 크기에 대해 서로 다른 이미지 품질과 형식의 이미지 사전 설정을 사용합니다. 작은 중단점의 경우, 이미지 제공이 6가지 색상으로만 압축된 GIF 이미지를 반환하도록 하는 낮은 품질의 사전 설정이 적용됩니다. 중간 중단점은 압축률이 높은 JPEG용으로 구성된 이미지 사전 설정을 사용합니다. 가장 큰 중단점은 무손실 PNG를 사용하는 고품질 이미지 사전 설정과 연결됩니다. 이러한 방법은 화면이 더 큰 디바이스가 더 큰 대역폭 및 처리 능력을 가정하는 것에 기초하여, 고품질의 이미지가 이러한 디바이스에 전달되도록 한다. </p> <p>URL을 클릭하여 웹 페이지를 열고 웹 브라우저 창의 크기를 큰 항목에서 작은 항목으로 변경하고 이미지 품질이 어떻게 감소하는지 확인합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/crops.html?lang=ko" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/crops.html?lang=ko </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/crops.html--> </p> </td> 
   <td colname="col2"> <p>이미지 사전 설정 외에도 특정 이미지 제공 명령을 중단점과 연결할 수 있습니다. 다음 예는 화면 이미지 크기가 작아짐에 따라 배너 이미지를 관심 영역으로 점진적으로 자를 수 있는 방법을 보여 줍니다. 여기서 가장 큰 중단점에는 이미지 제공 명령이 전혀 없으므로 배너 이미지가 완전히 표시됩니다. 중간 중단점에서 중간 정도의 자르기를 적용하여 "실행 중" 텍스트가 있는 실행자만 표시됩니다. 작은 중단점에서는 제품만 표시되도록 더 많은 자르기가 적용됩니다. </p> <p>URL을 클릭하여 웹 페이지를 열고 브라우저 창의 크기를 조정합니다. 더 큰 이미지에서 더 작은 크기로 갈수록 이미지가 어떻게 점진적으로 자르는지 확인하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/template.html?lang=ko" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/template.html?lang=ko </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/template.html--> </p> </td> 
   <td colname="col2"> <p>이미지 제공 템플릿에서 이미지 제공 명령을 사용하여 이미지 크기에 따라 특정 템플릿 매개 변수를 제어할 수도 있습니다. 다음 예제에서는 <span class="codeph"> $fontsize </span> 매개 변수를 사용하여 텍스트 오버레이의 글꼴 크기를 매개 변수화하는 이미지 제공 템플릿을 사용합니다. 응답 이미지는 텍스트가 항상 읽을 수 있도록 작은 이미지 크기에 대해 큰 글꼴 크기를 사용하도록 구성되어 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

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
