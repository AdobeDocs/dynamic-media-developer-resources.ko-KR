---
description: 회전판 뷰어에 대한 JavaScript API 참조.
solution: Experience Manager
title: getComponent**
feature: Dynamic Media Classic,Viewers,SDK/API,회전 배너
role: Developer,User
exl-id: 088d99d0-600d-4e47-85ea-a9769938b88b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 1%

---

# getComponent**{#getcomponent}

회전판 뷰어에 대한 JavaScript API 참조.

`getComponent(componentId)`

뷰어에서 사용하는 Viewer SDK 구성 요소에 대한 참조를 반환합니다. 웹 페이지에서는 이 메서드를 사용하여 기본 제공 뷰어의 동작을 확장하거나 사용자 지정할 수 있습니다. 이 메서드는 `initComplete` 뷰어 콜백이 실행된 후에만 호출하고, 그렇지 않으면 뷰어 논리로 구성 요소를 아직 만들지 않았을 수 있습니다.

## 매개 변수 {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

`*`componentID`*`  -  `{String}` 뷰어에서 사용하는 뷰어 SDK 구성 요소의 ID입니다. 이 뷰어는 다음 구성 요소 ID를 지원합니다.

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>구성 요소 ID </p> </th> 
   <th colname="col2" class="entry"> <p>Viewer SDK 구성 요소 클래스 이름 </p> </th> 
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
   <td colname="col1"> <p> <span class="codeph"> 회전판 보기  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.CarouselView  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imageMapEffect  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.image.mageMapEffect  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> controlBar  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ControlBar  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> setIndicator  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.SetIndicator  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nextButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.PanRightButton  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> prevButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.PanLeftButton  </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

SDK API를 사용할 때는 [Viewer SDK 네임스페이스](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-namespace.md)에 설명된 대로 올바른 정규화된 SDK 네임스페이스를 사용해야 합니다.

특정 구성 요소에 대한 자세한 내용은 뷰어 SDK API 설명서 를 참조하십시오.

## 반환 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` 뷰어 SDK 구성 요소에 대한 참조. `componentId` 이 지원되는 뷰어 구성 요소가 아니거나 뷰어 논리에 의해 구성 요소가 아직 만들어지지 않은 경우 이 메서드는 `null`을 반환합니다.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var carouselView = <instance>.getComponent("carouselView"); 
} 
})
```
