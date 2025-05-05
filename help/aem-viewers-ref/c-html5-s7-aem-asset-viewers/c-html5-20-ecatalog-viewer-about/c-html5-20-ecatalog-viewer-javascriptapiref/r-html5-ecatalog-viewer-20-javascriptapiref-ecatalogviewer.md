---
title: eCatalogViewer
description: eCatalog 뷰어에 대한 JavaScript API 참조입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 111699a3-8a70-4caf-b7da-7b594b785f7c
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 3%

---

# eCatalogViewer{#ecatalogviewer}

eCatalog 뷰어에 대한 JavaScript API 참조입니다.

`eCatalogViewer([config])`

생성자, eCatalog 뷰어 인스턴스를 만듭니다.

## 매개 변수 {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 구성 </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> 선택적 JSON 구성 개체로, 모든 뷰어 설정을 생성자에게 전달하고 개별 setter 메서드를 호출하지 않도록 합니다. 다음 속성을 포함합니다. </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <p> 뷰어가 삽입된 DOM 컨테이너(일반적으로 <span class="codeph"> DIV </span>)의 <span class="codeph"> containerId </span> - <span class="codeph"> {String} </span> ID. 이 메서드가 호출될 때까지 컨테이너 요소를 만들 필요는 없습니다. 그러나 <span class="codeph"> init() </span>을(를) 실행할 때는 컨테이너가 있어야 합니다. 필수. </p> </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <p> <span class="codeph"> 매개 변수 </span> - <span class="codeph"> {Object} </span> JSON 개체와 뷰어 구성 매개 변수 포함. 여기서 속성 이름은 뷰어별 구성 옵션 또는 SDK 한정자이고 해당 속성 값은 해당 설정 값입니다. 필수. </p> </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <p> <span class="codeph"> 처리기 </span> - <span class="codeph"> {Object} </span> 뷰어 이벤트 콜백이 있는 JSON 개체입니다. 여기서 속성 이름은 지원되는 뷰어 이벤트 이름이고 속성 값은 적절한 콜백에 대한 JavaScript 함수 참조입니다. 선택적. </p> <p>뷰어 이벤트에 대한 자세한 내용은 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-event-callbacks.md#concept-0bf5ff877043468db58ac62a92d002b6" format="dita" scope="local"> 이벤트 콜백 </a>을(를) 참조하십시오. </p> </li> 
      <li id="li_FE5B330E98834CB08C16FCA694F31BE3"> <p> 로컬라이제이션 데이터가 있는 <span class="codeph"> localizedText </span> - &lbrace; <span class="codeph"> Object </span> JSON 개체. 선택적. </p> <p>자세한 내용은 사용자 인터페이스 요소 </a>의 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> 지역화를 참조하십시오. </p> <p>개체 콘텐츠에 대한 자세한 내용은 <i>Viewer SDK 사용 안내서</i>와 예제를 참조하십시오. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 반환 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
var eCatalogViewer = new s7viewers.eCatalogViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"https://s7d1.scene7.com/is/image/" 
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
