---
description: eCatalog 뷰어에 대한 JavaScript API 참조입니다.
solution: Experience Manager
title: setHandler
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 33779874-2ab9-490a-8eaf-726adaa76327
TQID: 'https://experienceleague.adobe.com/K9tqgRqu3cKFndzAf-Wzp03EtMwUOhB51CtcQU0idiM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 9cbaa81231198414806938d25961167788e93789
workflow-type: tm+mt
source-wordcount: 87
ht-degree: 3%

---

# setHandler{#sethandlers}

eCatalog 뷰어에 대한 JavaScript API 참조입니다.

[!DNL `setHandlers(handlers)`]

0개 이상의 콜백 핸들러를 지정합니다. 이 메서드 호출은 해당 뷰어 인스턴스에 대해 이전에 할당된 이벤트 핸들러를 완전히 덮어씁니다. `init()` 전에 호출해야 합니다.

## 매개 변수 {#section-0cc9961784d04eb3b7d50011309b0119}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 처리기 </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> 뷰어 이벤트 콜백이 있는 JSON 개체. 여기서 속성 이름은 지원되는 뷰어 이벤트의 이름이고 속성 값은 적절한 콜백에 대한 JavaScript 함수 참조입니다. </p> <p>뷰어 이벤트에 대한 자세한 내용은 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-event-callbacks.md#concept-0bf5ff877043468db58ac62a92d002b6" format="dita" scope="local"> 이벤트 콜백 </a>을(를) 참조하십시오. </p> </td> 
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

