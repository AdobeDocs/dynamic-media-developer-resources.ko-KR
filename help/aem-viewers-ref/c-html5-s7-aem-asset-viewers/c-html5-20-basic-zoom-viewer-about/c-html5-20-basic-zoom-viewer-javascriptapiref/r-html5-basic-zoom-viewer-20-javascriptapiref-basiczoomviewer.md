---
title: 기본 확대/축소 뷰어
description: 기본 확대/축소 뷰어에 대한 JavaScript API 참조입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 320f740e-c6b9-44d6-9369-9c2ec31189c5
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 3%

---

# 기본 확대/축소 뷰어{#basiczoomviewer}

기본 확대/축소 뷰어에 대한 JavaScript API 참조입니다.

`BasicZoomViewer([config])`

생성자는 기본 확대/축소 뷰어 인스턴스를 만듭니다.

## 매개 변수 {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 구성 </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {object} </span> 선택적 JSON 구성 개체로, 개별 setter 메서드를 호출하지 않도록 모든 뷰어 설정을 생성자에게 전달할 수 있습니다. 다음 속성을 포함합니다. </p> <p> 
     <ul id="ul_789DBD5B72ED4C80B685455B0D59494D"> 
      <li id="li_28FDCB53E4AD4097A51F21B876C18FB1"> <p> 뷰어가 삽입된 DOM 컨테이너(일반적으로 <span class="codeph"> DIV </span>)의 <span class="codeph"> containerId {String} - </span> <span class="codeph"> </span> ID. 이 메서드가 호출될 때 컨테이너 요소를 만들 필요가 없습니다. 그러나 <span class="codeph"> init() </span>을(를) 실행할 때는 컨테이너가 있어야 합니다. 필수. </p> </li> 
      <li id="li_FDE00392DC1544ABBDD75F81EF814EF2"> <p> <span class="codeph"> 매개 변수 </span> - <span class="codeph"> {Object} </span> JSON 개체와 뷰어 구성 매개 변수 포함. 여기서 속성 이름은 뷰어별 구성 옵션 또는 SDK 수정자이고 해당 속성 값은 해당 설정 값입니다. 필수. </p> </li> 
      <li id="li_C534D5091CDA4717BCC48E3EBBF09AB8"> <p> <span class="codeph"> 처리기 </span> - <span class="codeph"> {Object} </span> 뷰어 이벤트 콜백이 있는 JSON 개체. 여기서 속성 이름은 지원되는 뷰어 이벤트 이름이고 속성 값은 적절한 콜백에 대한 JavaScript 함수 참조입니다. 선택적. </p> <p>뷰어 이벤트에 대한 자세한 내용은 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-event-callbacks.md#concept-8ba57cf86537401999514e1b221ec734" format="dita" scope="local"> 이벤트 콜백 </a>을(를) 참조하십시오. </p> </li> 
      <li id="li_528FE03845F847E08F964E38D6AB6E86"> <p> 로컬라이제이션 데이터가 있는 <span class="codeph"> localizedText </span> - <span class="codeph"> {Object} </span> JSON 개체. 선택적. </p> <p>자세한 내용은 사용자 인터페이스 요소 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local">의 </a> 지역화를 참조하십시오. </p> <p> 개체 콘텐츠에 대한 자세한 내용은 <i>Viewer SDK 사용 안내서</i> 및 예제를 참조하십시오. 선택적 </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 반환 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
var basicZoomViewer = new s7viewers.BasicZoomViewer({ 
 "containerId":"s7viewer", 
 "params":{ 
  "asset":"Scene7SharedAssets/Backpack_B", 
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
