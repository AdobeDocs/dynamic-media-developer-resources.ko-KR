---
description: 인라인 확대/축소 뷰어에 대한 JavaScript API 참조입니다.
seo-description: 인라인 확대/축소 뷰어에 대한 JavaScript API 참조입니다.
seo-title: FlyoutViewer
solution: Experience Manager
title: FlyoutViewer
topic: Dynamic media
uuid: 23617eda-f4c9-4908-9f63-593849c12fc7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutViewer{#flyoutviewer}

인라인 확대/축소 뷰어에 대한 JavaScript API 참조입니다.

`FlyoutViewer([config])`

생성자;새 인라인 확대/축소 뷰어 인스턴스를 만듭니다.

## 매개 변수 {#section-8bc3d1424c8444f193716fc8d9975765}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 구성 </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> 선택적 JSON 구성 개체를 사용하면 모든 뷰어 설정이 생성자에 전달되고 개별 setter 메서드를 호출하지 않아도 됩니다. 다음 속성을 포함합니다. </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <span class="codeph"> containerID </span> - <span class="codeph"> {String} </span> 뷰어가 삽입된 DOM 컨테이너( <span class="codeph"> 일반적으로 DIV </span>)의 ID. 이 메서드를 호출할 때까지 컨테이너 요소를 만들 필요는 없습니다. 그러나 <span class="codeph"> init()를 </span> 실행할 때는 컨테이너가 존재해야 합니다. 필수. </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <span class="codeph"> params </span> - <span class="codeph"> {Object} </span> JSON 개체(속성 이름이 뷰어 특정 구성 옵션 또는 SDK 수정자 중 하나이며 해당 속성의 값은 해당 설정 값입니다. 필수. </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <span class="codeph"> 핸들러 </span> - <span class="codeph"> {Object} </span> 뷰어 이벤트 콜백이 있는 JSON 개체. 여기서 속성 이름은 지원되는 뷰어 이벤트의 이름이고 속성 값은 해당 콜백에 대한 JavaScript 함수 참조입니다. 선택 사항입니다. <p>뷰어 이벤트에 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-event-callbacks.md#concept-53eb01d28189437790268da4929f2a10" format="dita" scope="local"> 대한 자세한 내용은 이벤트 콜백을 </a> 참조하십시오. </p> </li> 
      <li id="li_218F9597A60249AEBA43A9E86EAFF8BA"> <p> <span class="codeph"> localizedText </span> - 현지화 데이터가 있는 { <span class="codeph"> Object </span>} JSON 개체. 선택 사항입니다. </p> <p>자세한 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27" format="dita" scope="local"> 내용은 사용자 인터페이스 요소의 현지화를 </a> 참조하십시오. </p> <p>개체 <i>컨텐츠에 대한 자세한</i> 내용은 Viewer SDK 사용 안내서 및 예제를 참조하십시오. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var inlineZoomViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
"config" : "Scene7SharedAssets/Universal_HTML5_Zoom_Inline", 
"contenturl" : "http://s7d1.scene7.com/is/content/", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
}, 
"handlers":{ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
}, 
"localizedTexts":{ 
"en":{ 
"FlyoutZoomView.TIP_BUBBLE_OVER":"Mouse over to zoom" 
}, 
"fr":{ 
"FlyoutZoomView.TIP_BUBBLE_OVER":"Passez la souris sur pour zoomer" 
}, 
defaultLocale:"en" 
} 
});
```

