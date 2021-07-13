---
description: 비디오 이미지 뷰어에 대한 JavaScript API 참조.
solution: Experience Manager
title: setParams
feature: Dynamic Media Classic,Viewers,SDK/API,대화형 이미지
role: Developer,User
exl-id: 6a09e3bc-e79c-4206-be42-0c6ae3d91590
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 2%

---

# setParams{#setparams}

비디오 이미지 뷰어에 대한 JavaScript API 참조.

` setParams( *`params`*)`

하나 이상의 매개 변수를 지정된 값으로 설정합니다. 메서드 인수 구문은 URL 쿼리 문자열과 동일합니다. 즉, 이름=값 쌍을 `&`과(와) 함께 나타냅니다. 쿼리 문자열과 마찬가지로 이름과 값은 UTF8을 사용하여 퍼센트 인코딩됩니다. `init()`을 호출하기 전에 이 매개 변수를 호출해야 합니다.

이 메서드는 뷰어 구성 정보가 `config` JSON 개체와 함께 생성자에 전달된 경우 선택 사항입니다.

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)도 참조하십시오.

## 매개 변수 {#section-add05f3d7ca0426897bd74bf7ac9b9cd}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> params</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=value 매개 변수 쌍이  <span class="codeph"> &amp;</span>로 구분됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 반환 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("ZoomView.fmt=png&ZoomView.iscommand=op_sharpen%3d1")
```
