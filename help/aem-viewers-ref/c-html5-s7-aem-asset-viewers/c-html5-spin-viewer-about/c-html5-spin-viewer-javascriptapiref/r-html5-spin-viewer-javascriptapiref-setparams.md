---
description: 스핀 뷰어용 JavaScript API 참조.
seo-description: 스핀 뷰어용 JavaScript API 참조.
seo-title: setParams
solution: Experience Manager
title: setParams
topic: Dynamic media
uuid: f0eedfbd-eb32-49db-bca4-cc7b14d5495e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setParams{#setparams}

스핀 뷰어용 JavaScript API 참조.

` setParams( *`params`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 매개 변수</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=value 매개 변수 쌍은 <span class="codeph"> &amp;</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

하나 이상의 매개 변수를 지정된 값으로 설정합니다. 메서드 인수 구문은 URL 쿼리 문자열과 동일합니다. 즉, 로 구분된 name=value 쌍을 나타냅니다 `&`. 쿼리 문자에서와 마찬가지로 이름과 값은 UTF8을 사용하여 퍼센트 인코딩됩니다. 호출하기 `init()`전에 이 매개 변수를 호출해야 합니다.

이 메서드는 뷰어 구성 정보가 JSON 개체와 함께 생성자에 전달될 경우 `config` 선택 사항입니다.

또한 [init](../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-javascriptapiref/r-html5-spin-viewer-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae)를 참조하십시오.

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("SpinView.zoomstep=2,3&SpinView.iscommand=op_sharpen%3d1")
```

