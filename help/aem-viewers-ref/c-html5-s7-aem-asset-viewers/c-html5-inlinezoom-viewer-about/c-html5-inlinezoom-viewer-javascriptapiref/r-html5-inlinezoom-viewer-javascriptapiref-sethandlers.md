---
title: setHandler
description: 인라인 확대/축소 뷰어에 대한 JavaScript API 참조입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 233fadf5-4b09-406d-959b-c2c9c4524021
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 3%

---

# setHandler{#sethandlers}

인라인 확대/축소 뷰어에 대한 JavaScript API 참조입니다.

`setHandlers(handlers)`

0개 이상의 콜백 핸들러를 지정합니다. 이 메서드 호출은 해당 뷰어 인스턴스에 대해 이전에 할당된 이벤트 핸들러를 완전히 덮어씁니다. `init()` 전에 호출해야 합니다.

## 매개 변수 {#section-0cc9961784d04eb3b7d50011309b0119}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 처리기 </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> 뷰어 이벤트 콜백이 있는 JSON 개체. 여기서 속성 이름은 지원되는 뷰어 이벤트의 이름이고 속성 값은 적절한 콜백에 대한 JavaScript 함수 참조입니다. </p> <p>뷰어 이벤트에 대한 자세한 내용은 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-event-callbacks.md#concept-53eb01d28189437790268da4929f2a10" format="dita" scope="local"> 이벤트 콜백 </a>을(를) 참조하십시오. </p> </td> 
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
