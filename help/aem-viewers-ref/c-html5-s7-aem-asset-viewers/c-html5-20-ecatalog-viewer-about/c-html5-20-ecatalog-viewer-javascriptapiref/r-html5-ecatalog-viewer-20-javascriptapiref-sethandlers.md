---
title: setHandler
description: eCatalog 뷰어에 대한 JavaScript API 참조입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: a6709da7-1fa2-421b-8c99-a4ccea83c600
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 3%

---

# setHandler{#sethandlers}

eCatalog 뷰어에 대한 JavaScript API 참조입니다.

`setHandlers(handlers)`

0개 이상의 콜백 핸들러를 지정합니다. 이 메서드 호출은 해당 뷰어 인스턴스에 대해 이전에 할당된 이벤트 핸들러를 완전히 덮어씁니다. 전에 호출해야 함 `init()`.

## 매개 변수 {#section-0cc9961784d04eb3b7d50011309b0119}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 핸들러 </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> 속성 이름이 지원되는 뷰어 이벤트 이름이고 속성 값이 적절한 콜백에 대한 JavaScript 함수 참조인 뷰어 이벤트 콜백이 있는 JSON 개체입니다. </p> <p>다음을 참조하십시오 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-event-callbacks.md#concept-0bf5ff877043468db58ac62a92d002b6" format="dita" scope="local"> 이벤트 콜백 </a> 뷰어 이벤트에 대한 자세한 정보. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 반환 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
})
```
