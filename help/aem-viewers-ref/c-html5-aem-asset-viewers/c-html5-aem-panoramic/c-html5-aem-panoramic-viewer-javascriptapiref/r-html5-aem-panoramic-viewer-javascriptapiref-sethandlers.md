---
title: setHandler
description: 파노라마 뷰어에 대한 JavaScript API 참조
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: 90775d4a-386b-4b56-b75e-8afafe749645
source-git-commit: 8aebcacd5abdc23565aab1bc3506c36f055b6439
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 3%

---

# setHandler{#sethandlers}

파노라마 뷰어에 대한 JavaScript API 참조

`setHandlers(handlers)`

0개 이상의 콜백 핸들러를 지정합니다. 이 메서드 호출은 해당 뷰어 인스턴스에 대해 이전에 할당된 이벤트 핸들러를 완전히 덮어씁니다. 전에 호출해야 함 `init()`.

## 매개 변수 {#section-b60f082cca1542748b605689b1d43f8a}

<table id="table_98A620DAE2C340FA97BF7204AE023CC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 핸들러 </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> 속성 이름이 지원되는 뷰어 이벤트 이름이고 속성 값이 적절한 콜백에 대한 JavaScript 함수 참조인 뷰어 이벤트 콜백이 있는 JSON 개체입니다. </p> <p>뷰어 이벤트에 대한 자세한 내용은 이벤트 콜백 섹션을 참조하십시오. </p> </td> 
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
