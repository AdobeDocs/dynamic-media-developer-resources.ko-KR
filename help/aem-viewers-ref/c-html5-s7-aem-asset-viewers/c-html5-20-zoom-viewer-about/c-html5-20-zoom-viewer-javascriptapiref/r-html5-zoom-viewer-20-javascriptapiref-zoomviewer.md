---
title: ZoomViewer
description: 확대/축소 뷰어에 대한 JavaScript API 참조.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: fa52a017-0748-4e4f-8d91-ad1529fbfbdb
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 3%

---

# ZoomViewer{#zoomviewer}

확대/축소 뷰어에 대한 JavaScript API 참조.

`ZoomViewer([config])`

생성자는 확대/축소 뷰어 인스턴스를 만듭니다.

## 매개 변수 {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {object} </span> 선택적 JSON 구성 개체를 사용하면 개별 setter 메서드를 호출하지 않도록 모든 뷰어 설정을 생성자에 전달할 수 있습니다. 다음 속성을 포함합니다. </p> <p> 
     <ul id="ul_789DBD5B72ED4C80B685455B0D59494D"> 
      <li id="li_28FDCB53E4AD4097A51F21B876C18FB1"> <span class="codeph"> containerId </span> - <span class="codeph"> {String} </span> DOM 컨테이너 ID(일반적으로 <span class="codeph"> DIV </span>)에 뷰어를 삽입합니다. 이 메서드가 호출될 때 컨테이너 요소를 만들 필요가 없습니다. 단, 컨테이너는 다음과 같은 경우에 존재해야 합니다. <span class="codeph"> init() </span> 가 실행되었습니다. 필수. </li> 
      <li id="li_FDE00392DC1544ABBDD75F81EF814EF2"> <span class="codeph"> 매개 변수 </span> - <span class="codeph"> {Object} </span> 속성 이름이 뷰어별 구성 옵션 또는 SDK 수정자이고 해당 속성 값이 해당 설정 값인 뷰어 구성 매개 변수가 있는 JSON 개체입니다. 필수. </li> 
      <li id="li_C534D5091CDA4717BCC48E3EBBF09AB8"> <span class="codeph"> 핸들러 </span> - <span class="codeph"> {Object} </span> 속성 이름이 지원되는 뷰어 이벤트 이름이고 속성 값이 적절한 콜백에 대한 JavaScript 함수 참조인 뷰어 이벤트 콜백이 있는 JSON 개체입니다. 선택적. <p>다음을 참조하십시오 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> 이벤트 콜백 </a> 뷰어 이벤트에 대한 자세한 정보. </p> </li> 
      <li id="li_1D181A6B1D434B29B09AFD3F4BE059BD"> <span class="codeph"> 지역화된 텍스트 </span> - <span class="codeph"> {Object} </span> 로컬라이제이션 데이터가 있는 JSON 개체입니다. 선택적. <p>다음을 참조하십시오 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> 사용자 인터페이스 요소의 현지화 </a> 추가 정보. </p> <p>참조: <i>Viewer SDK 사용 안내서</i> 객체의 컨텐트에 대한 자세한 내용은 예제를 참조하십시오. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 반환 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
var zoomViewer = new s7viewers.ZoomViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
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
