---
title: setParam
description: 혼합 미디어 뷰어에 대한 JavaScript API 참조입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 610a5a7d-1314-48bc-a640-319139d64adc
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 2%

---

# setParam{#setparam}

혼합 미디어 뷰어에 대한 JavaScript API 참조입니다.

` setParam( *`이름, 값`*)`

viewer 매개 변수를 지정된 값으로 설정합니다. 매개 변수는 뷰어별 구성 옵션 또는 소프트웨어 개발 키트 수정자입니다. 이 매개 변수는 `init()` 전에 호출됩니다. 뷰어 구성 정보가 `config` JSON 개체와 함께 생성자에 전달되는 경우 이 메서드는 선택 사항입니다.

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae)도 참조하세요.

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 이름 </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> 매개 변수 이름. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 값 </span> </span> </p> </td> 
   <td colname="col2"> <p> 매개 변수의 <span class="codeph"> {string} </span> 값입니다. 값은 퍼센트 인코딩할 수 없습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 반환 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "customStyle.css")
```
