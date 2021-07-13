---
description: 스핀 뷰어에 대한 JavaScript API 참조.
solution: Experience Manager
title: SpinViewer
feature: Dynamic Media Classic,Viewers,SDK/API,스핀 세트
role: Developer,User
exl-id: 0cfde665-c578-41a0-a428-0db3cbdac6ae
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 3%

---

# SpinViewer{#spinviewer}

스핀 뷰어에 대한 JavaScript API 참조.

`SpinViewer([config])`

생성자에서 새 스핀 뷰어 인스턴스를 만듭니다.

## 매개 변수 {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object}  </span> 선택적 JSON 구성 개체를 사용하면 모든 뷰어 설정이 생성자에 전달되고 개별 setter 메서드를 호출하지 않도록 할 수 있습니다. 다음 속성을 포함합니다. </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <p> <span class="codeph"> containerId  </span> -  <span class="codeph"> {String}  </span> 뷰어가 삽입되는 DOM 컨테이너(일반적으로  <span class="codeph"> DIV </span>)의 ID입니다. 이 메서드가 호출될 때까지 컨테이너 요소를 만들 필요가 없습니다. 그러나 <span class="codeph"> init() </span> 가 실행될 때는 컨테이너가 있어야 합니다. 필수. </p> </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <p> <span class="codeph"> params  </span> -  <span class="codeph"> {Object}  </span> JSON 개체(속성 이름이 뷰어 특정 구성 옵션 또는 SDK 수정자 중 하나이고 해당 속성 값은 해당 설정 값입니다. 필수. </p> </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <p> <span class="codeph"> 핸들러  </span> -  <span class="codeph"> {Object}  </span> 뷰어 이벤트 콜백이 있는 JSON 개체. 여기서 속성 이름은 지원되는 뷰어 이벤트의 이름이고, 속성 값은 적절한 콜백에 대한 JavaScript 함수 참조입니다. 선택 사항입니다. </p> <p>뷰어 이벤트에 대한 자세한 내용은 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-event-callbacks.md#concept-9c553c80eefd422faacf6522c69804bf" format="dita" scope="local"> 이벤트 콜백 </a> 을 참조하십시오. </p> </li> 
      <li id="li_643787FB4A424D0AB6B8E12F44C3A9AC"> <p> <span class="codeph"> 로컬라이제이션된  </span> -  <span class="codeph"> {Object}  </span> JSON 개체에 현지화 데이터가 있습니다. 선택 사항입니다. </p> <p>자세한 내용은 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-localization.md#concept-e35c15c9e82648328806cdc6aa255d98" format="dita" scope="local"> 사용자 인터페이스 요소 현지화 </a> 를 참조하십시오. </p> <p>개체 컨텐츠에 대한 자세한 내용은 <i>Viewer SDK 사용 안내서</i> 및 예제를 참조하십시오. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 반환 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var spinViewer = new s7viewers.SpinViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/SpinSet_Sample", 
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
