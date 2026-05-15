---
title: setParam
description: Spin Viewer에 대한 JavaScript API 참조.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 16d1d2cd-f58f-4ac3-b89f-f2f12fee231d
TQID: 'https://experienceleague.adobe.com/R0HdN4vDg-LC6em1E3KdzQI5d4uwttBhK1sQPI77Dw8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 83
ht-degree: 2%

---

# setParam{#setparam}

Spin Viewer에 대한 JavaScript API 참조.

` setParam( *`이름, 값`*)`

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

viewer 매개 변수를 지정된 값으로 설정합니다. 매개 변수는 뷰어별 구성 옵션 또는 소프트웨어 개발 키트 수정자입니다. 이 매개 변수는 `init()` 전에 호출됩니다.

뷰어 구성 정보가 `config` JSON 개체와 함께 생성자에 전달되는 경우 이 메서드는 선택 사항입니다.

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-javascriptapiref/r-html5-spin-viewer-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae)도 참조하세요.

## 반환 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "customStyle.css")
```
