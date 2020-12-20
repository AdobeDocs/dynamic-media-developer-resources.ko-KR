---
description: 대화형 비디오 뷰어용 JavaScript API 참조
seo-description: 대화형 비디오 뷰어용 JavaScript API 참조
seo-title: setHandlers
solution: Experience Manager
title: setHandlers
topic: Dynamic media
uuid: f33df5a9-e323-4dff-b792-88d778332c75
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 3%

---


# setHandlers{#sethandlers}

대화형 비디오 뷰어용 JavaScript API 참조

`setHandlers(handlers)`

콜백 핸들러를 0개 이상 지정합니다. 이 메서드를 호출하면 해당 뷰어 인스턴스에 대해 이전에 할당된 이벤트 핸들러를 덮어씁니다. `init()` 이전에 호출해야 합니다.

## 매개 변수 {#section-b60f082cca1542748b605689b1d43f8a}

<table id="table_98A620DAE2C340FA97BF7204AE023CC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 핸들러  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 뷰어 이벤트 콜백이 있는 {Object}  </span> JSON 개체. 여기서 속성 이름은 지원되는 뷰어 이벤트의 이름이고 속성 값은 해당 콜백에 대한 JavaScript 함수 참조입니다. </p> <p>뷰어 이벤트에 대한 자세한 내용은 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> 이벤트 콜백 </a>을 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

## {#section-1d3cf85bc7cc4dfe9670e038d02b9101} 반환

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
})
```

