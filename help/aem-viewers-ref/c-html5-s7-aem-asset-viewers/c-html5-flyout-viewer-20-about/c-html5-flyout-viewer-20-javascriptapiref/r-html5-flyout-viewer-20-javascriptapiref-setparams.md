---
description: 플라이아웃 뷰어에 대한 JavaScript API 참조입니다.
seo-description: 플라이아웃 뷰어에 대한 JavaScript API 참조입니다.
seo-title: setParams
solution: Experience Manager
title: setParams
topic: Dynamic Media
uuid: 12a513d3-32a9-411d-965f-f0eaf553d98d
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 1%

---


# setParams{#setparams}

플라이아웃 뷰어에 대한 JavaScript API 참조입니다.

` setParams( *`params`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> params</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=value 매개 변수 쌍은  <span class="codeph"> &amp;</span>로 구분됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

하나 이상의 매개 변수를 지정된 값으로 설정합니다. 메서드 인수 구문은 URL 쿼리 문자열과 동일합니다. 즉, 이름=값 쌍을 `&`으로 구분하여 나타냅니다. 쿼리 문자열과 마찬가지로 이름 및 값은 UTF8을 사용하여 퍼센트 인코딩됩니다. `init()`을(를) 호출하기 전에 이 매개 변수를 호출해야 합니다. 이 메서드는 뷰어 구성 정보가 `config` JSON 개체와 함께 생성자에 전달될 경우 선택 사항입니다.

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-init.md#reference-8651640683fc4a538bfb660709d1a463)도 참조하십시오.

## {#section-1d3cf85bc7cc4dfe9670e038d02b9101} 반환

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("FlyoutZoomView.zoomfactor=2,3&Swatches.iscommand=op_sharpen%3d1")
```

