---
description: eCatalog SearchViewer용 JavaScript API 참조
seo-description: eCatalog SearchViewer용 JavaScript API 참조
seo-title: eCatalogSearchViewer
solution: Experience Manager
title: eCatalogSearchViewer
topic: Dynamic media
uuid: 304724aa-3f50-46de-97d0-48e8c81401ed
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# eCatalogSearchViewer{#ecatalogsearchviewer}

eCatalog SearchViewer용 JavaScript API 참조

[!DNL `eCatalogSearchViewer([config])`]

생성자가 새 eCatalog 검색 뷰어 인스턴스를 만듭니다.

## 매개 변수 {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 구성 </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> 선택적 JSON 구성 개체를 사용하면 모든 뷰어 설정이 생성자에 전달되고 개별 setter 메서드를 호출하지 않아도 됩니다. 다음 속성을 포함합니다. </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <p> <span class="codeph"> containerID </span> - <span class="codeph"> {String} </span> 뷰어가 삽입된 DOM 컨테이너( <span class="codeph"> 일반적으로 DIV </span>)의 ID. 이 메서드를 호출할 때까지 컨테이너 요소를 만들 필요는 없습니다. 그러나 <span class="codeph"> init()를 </span> 실행할 때는 컨테이너가 존재해야 합니다. 필수. </p> </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <p> <span class="codeph"> params </span> - <span class="codeph"> {Object} </span> JSON 개체(속성 이름이 뷰어 특정 구성 옵션 또는 SDK 수정자 중 하나이며 해당 속성의 값은 해당 설정 값입니다. 필수. </p> </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <p> <span class="codeph"> 핸들러 </span> - <span class="codeph"> {Object} </span> 뷰어 이벤트 콜백이 있는 JSON 개체. 여기서 속성 이름은 지원되는 뷰어 이벤트의 이름이고 속성 값은 해당 콜백에 대한 JavaScript 함수 참조입니다. 선택 사항입니다. </p> <p>뷰어 이벤트에 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-event-callbacks.md#concept-0bf5ff877043468db58ac62a92d002b6" format="dita" scope="local"> 대한 자세한 내용은 이벤트 콜백을 </a> 참조하십시오. </p> </li> 
      <li id="li_FE5B330E98834CB08C16FCA694F31BE3"> <p> <span class="codeph"> localizedText </span> - 현지화 데이터가 있는 { <span class="codeph"> Object </span>} JSON 개체. 선택 사항입니다. </p> <p>자세한 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> 내용은 사용자 인터페이스 요소의 현지화를 </a> 참조하십시오. </p> <p>개체 <i>컨텐츠에 대한 자세한</i> 내용은 Viewer SDK 사용 안내서 및 예제를 참조하십시오. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "searchserverurl":"http://s7search1.scene7.com/s7search/" 
}, 
"handlers":{ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
}, 
"localizedTexts":{ 
"en":{ 
"CloseButton.TOOLTIP":"Close" 
}, 
"fr":{ 
"CloseButton.TOOLTIP":"Fermer" 
}, 
defaultLocale:"en" 
} 
});
```

