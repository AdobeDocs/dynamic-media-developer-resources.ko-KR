---
title: setParams
description: 인라인 확대/축소 뷰어에 대한 JavaScript API 참조.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: eb3298da-f19d-4013-8192-c51144d8b866
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 2%

---

# setParams{#setparams}

인라인 확대/축소 뷰어에 대한 JavaScript API 참조.

` setParams( *`params`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> params</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=값 매개 변수 쌍이 <span class="codeph"> &amp;</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

하나 이상의 매개 변수를 지정된 값으로 설정합니다. 메서드 인수 구문은 URL 쿼리 문자열과 동일합니다. 즉, 와 구분된 이름=값 쌍을 나타냅니다 `&`. 쿼리 문자열, 이름 및 값과 동일한 값은 UTF8을 사용하여 퍼센트 인코딩됩니다. 호출하기 전에 `init()`로 지정하는 경우 이 매개 변수를 호출해야 합니다. 이 메서드는 뷰어 구성 정보가 `config` 생성자에 대한 JSON 개체.

참조 - [init](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-init.md#reference-8651640683fc4a538bfb660709d1a463).

## 반환 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("FlyoutZoomView.zoomfactor=2,3&Swatches.iscommand=op_sharpen%3d1")
```
