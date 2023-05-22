---
title: setParams
description: 플라이아웃 뷰어에 대한 JavaScript API 참조.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: bd26292d-f9c6-4e67-8cc1-c74336d50860
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 2%

---

# setParams{#setparams}

플라이아웃 뷰어에 대한 JavaScript API 참조.

` setParams( *`매개 변수`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 매개 변수</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> 다음으로 구분된 name=value 매개 변수 쌍 <span class="codeph"> 및</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

하나 이상의 매개 변수를 지정된 값으로 설정합니다. 메서드 인수 구문은 URL 쿼리 문자열과 동일합니다. 즉, 다음과 같이 구분된 name=value 쌍을 나타냅니다. `&`. 쿼리 문자열과 마찬가지로 이름 및 값은 UTF8을 사용하여 퍼센트 인코딩됩니다. 통화하기 전에 `init()`, 이 매개 변수를 호출해야 합니다. 뷰어 구성 정보가 로 전달되는 경우 이 메서드는 선택 사항입니다. `config` 생성자에 대한 JSON 개체입니다.

참조: [init](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-init.md#reference-8651640683fc4a538bfb660709d1a463).

## 반환 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("FlyoutZoomView.zoomfactor=2,3&Swatches.iscommand=op_sharpen%3d1")
```
