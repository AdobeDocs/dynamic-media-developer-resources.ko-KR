---
description: 혼합 미디어 뷰어에 대한 JavaScript API 참조.
solution: Experience Manager
title: setHandlers
feature: Dynamic Media Classic,Viewers,SDK/API,혼합 미디어 집합
role: Developer,User
exl-id: e30f1b73-1dba-4d4c-9e90-f343ca404550
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 3%

---

# setHandlers{#sethandlers}

혼합 미디어 뷰어에 대한 JavaScript API 참조.

`setHandlers(handlers)`

콜백 처리기를 0개 이상 지정합니다. 이 메서드 호출은 해당 뷰어 인스턴스에 대해 이전에 할당한 이벤트 핸들러를 완전히 덮어씁니다. `init()` 앞에 를 호출해야 합니다.

## 매개 변수 {#section-0cc9961784d04eb3b7d50011309b0119}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 핸들러  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 뷰어 이벤트 콜백이 있는 {Object}  </span> JSON 개체. 여기서 속성 이름은 지원되는 뷰어 이벤트의 이름이고 속성 값은 적절한 콜백에 대한 JavaScript 함수 참조입니다. </p> <p>뷰어 이벤트에 대한 자세한 내용은 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-event-callbacks.md#concept-273d2cddbb7144e284b618ffaf3deabc" format="dita" scope="local"> 이벤트 콜백 </a> 을 참조하십시오. </p> </td> 
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
