---
description: 기본 확대/축소 뷰어용 JavaScript API 참조
seo-description: 기본 확대/축소 뷰어용 JavaScript API 참조
seo-title: getComponent
solution: Experience Manager
title: getComponent
topic: Dynamic media
uuid: 3e9f4baf-4914-42a8-a1bf-5756cbbd407b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 1%

---


# getComponent{#getcomponent}

기본 확대/축소 뷰어용 JavaScript API 참조

`getComponent(componentId)`

뷰어에서 사용하는 뷰어 SDK 구성 요소에 대한 참조를 반환합니다. 웹 페이지에서는 이 방법을 사용하여 기본 뷰어의 비헤이비어를 확장하거나 사용자 지정할 수 있습니다. 이 메서드는 `initComplete` 뷰어 콜백이 실행된 후에만 호출하며, 그렇지 않으면 뷰어 논리로 구성 요소를 아직 만들 수 없습니다.

## 매개 변수 {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

` *`componentID`*`   `{String}` - 뷰어에서 사용하는 뷰어 SDK 구성 요소의 ID입니다. 이 뷰어는 다음 구성 요소 ID를 지원합니다.

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>구성 요소 ID </p> </th> 
   <th colname="col2" class="entry"> <p>뷰어 SDK 구성 요소 클래스 이름 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parameterManager  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.ParameterManager  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 컨테이너 </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.Container  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mediaSet  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.MediaSet  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomView  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.image.ZoomView  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomInButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ZoomInButton  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomOutButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ZoomOutButton  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomResetButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ZoomResetButton  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> fullScreenButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.FullScreenButton  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> closeButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.CloseButton  </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

SDK API 작업 시 뷰어 SDK 네임스페이스에 설명된 대로 올바르게 정규화된 SDK 네임스페이스를 사용해야 합니다

특정 구성 요소에 대한 자세한 내용은 Viewer SDK API 설명서를 참조하십시오.

## {#section-1d3cf85bc7cc4dfe9670e038d02b9101} 반환

`{Object}` 뷰어 SDK 구성 요소에 대한 참조입니다. `componentId`이(가) 지원되는 뷰어 구성 요소가 아니거나 뷰어 논리로 구성 요소를 아직 만들지 않은 경우 이 메서드는 `null`을 반환합니다.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var zoomView = <instance>.getComponent("zoomView"); 
} 
})
```

