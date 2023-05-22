---
title: setParams
description: 기본 확대/축소 뷰어에 대한 JavaScript API 참조입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: f142dd72-5e45-44f6-a79b-3eaf6a310bde
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 2%

---

# setParams{#setparams}

기본 확대/축소 뷰어에 대한 JavaScript API 참조입니다.

` setParams( *`매개 변수`*)`

하나 이상의 매개 변수를 지정된 값으로 설정합니다. 메서드 인수 구문은 URL 쿼리 문자열과 동일합니다. 즉, 다음과 같이 구분된 name=value 쌍을 나타냅니다. `&`. 쿼리 문자열에서와 같이, 이름과 값은 UTF8을 사용하여 퍼센트 인코딩됩니다. 통화하기 전에 `init()`, 이 매개 변수를 호출해야 합니다.

뷰어 구성 정보가 로 전달된 경우 이 메서드는 선택 사항입니다 `config` 생성자에 대한 JSON 개체입니다.

참조: [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-javascriptapiref/r-html5-basic-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 매개 변수</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> 다음으로 구분된 name=value 매개 변수 쌍 <span class="codeph"> 및</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 반환 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("ZoomView.zoomfactor=2,3&ZoomView.iscommand=op_sharpen%3d1")
```
