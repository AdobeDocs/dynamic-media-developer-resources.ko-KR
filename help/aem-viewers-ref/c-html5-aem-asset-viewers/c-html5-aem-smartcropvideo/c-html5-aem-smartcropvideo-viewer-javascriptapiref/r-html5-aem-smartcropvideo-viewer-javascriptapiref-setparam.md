---
description: 스마트 자르기 비디오 뷰어에 대한 JavaScript API 참조.
solution: Experience Manager
title: setParam
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: b28ffb51-1091-4f2e-b12d-904218daf117
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 2%

---

# setParam{#setparam}

스마트 자르기 비디오 뷰어에 대한 JavaScript API 참조.

` setParam( *`이름, 값`*)`

뷰어 매개 변수를 지정된 값으로 설정합니다. 매개 변수는 뷰어별 구성 옵션 또는 소프트웨어 개발 키트 수정자입니다. 이 매개 변수는 전에 호출됩니다 `init()`.

이 메서드는 뷰어 구성 정보가 `config` 생성자에 대한 JSON 개체.

참조 - [init](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 이름 </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> 매개 변수의 이름입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> value </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> 매개 변수의 값입니다. 값을 퍼센트 인코딩할 수 없습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 반환 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "customStyle.css")
```
