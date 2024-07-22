---
title: setParams
description: eCatalog 뷰어에 대한 JavaScript API 참조입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: a93c14e8-d322-4630-9334-1b4413f1e443
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 2%

---

# setParams{#setparams}

eCatalog 뷰어에 대한 JavaScript API 참조입니다.

` setParams( *`매개 변수`*)`

하나 이상의 매개 변수를 지정된 값으로 설정합니다. 메서드 인수 구문은 URL 쿼리 문자열과 동일합니다. 즉, `&`(으)로 구분된 이름=값 쌍을 나타냅니다. 쿼리 문자열에서와 마찬가지로, 이름과 값은 UTF8을 사용하여 퍼센트 인코딩됩니다. `init()`을(를) 호출하기 전에 이 매개 변수를 호출해야 합니다.

뷰어 구성 정보가 `config` JSON 개체와 함께 생성자에 전달되는 경우 이 메서드는 선택 사항입니다.

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)도 참조하세요.

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 매개 변수</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> 이름=값 매개 변수 쌍이 <span class="codeph"> &amp;</span>(으)로 구분되었습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 반환 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("PageView.zoomstep=2,3&PageView.iscommand=op_sharpen%3d1")
```
