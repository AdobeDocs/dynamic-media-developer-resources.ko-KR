---
description: 인라인 확대/축소 뷰어에 대한 JavaScript API 참조
solution: Experience Manager
title: getComponent
feature: Dynamic Media Classic,뷰어,SDK/API,인라인 확대/축소
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 1%

---


# getComponent{#getcomponent}

인라인 확대/축소 뷰어에 대한 JavaScript API 참조

`getComponent(componentId)`

뷰어에서 사용하는 뷰어 SDK 구성 요소에 대한 참조를 반환합니다. 웹 페이지에서는 이 방법을 사용하여 기본 뷰어의 비헤이비어를 확장하거나 사용자 지정할 수 있습니다. `initComplete` 뷰어 콜백이 실행된 후에만 이 메서드를 호출합니다.그렇지 않으면 뷰어 논리로 구성 요소를 아직 만들 수 없습니다.

## 매개 변수 {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

`*`componentID`*`   `{String}` - 뷰어에서 사용하는 뷰어 SDK 구성 요소의 ID입니다. 이 뷰어는 다음 구성 요소 ID를 지원합니다.

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
   <td colname="col1"> <p> <span class="codeph"> 플라이아웃  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.image.FlyoutZoomView  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 견본  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.Swatches  </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

SDK API 작업 시 [뷰어 SDK](../../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-namespace.md#concept-5af3b472b320496d87735ea612edda80)에 설명된 대로 올바른 정규화된 SDK 네임스페이스를 사용해야 합니다.

특정 구성 요소에 대한 자세한 내용은 Viewer SDK 설명서를 참조하십시오.

## {#section-1d3cf85bc7cc4dfe9670e038d02b9101} 반환

`{Object}` 뷰어 SDK 구성 요소에 대한 참조입니다. `componentId`이(가) 지원되는 뷰어 구성 요소가 아니거나 뷰어 논리로 구성 요소를 아직 만들지 않은 경우 이 메서드는 `null`을 반환합니다.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var flyoutZoomView = <instance>.getComponent("flyout"); 
} 
})
```

