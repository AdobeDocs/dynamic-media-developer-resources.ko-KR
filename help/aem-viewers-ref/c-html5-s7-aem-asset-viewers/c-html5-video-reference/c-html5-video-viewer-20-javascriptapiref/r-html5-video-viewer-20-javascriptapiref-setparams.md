---
title: setParams
description: 비디오 뷰어에 대한 JavaScript API 참조.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 76bad894-bfb8-4d79-b3ff-c2497c68e5e8
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 2%

---

# setParams{#setparams}

비디오 뷰어에 대한 JavaScript API 참조.

` setParams( *`params`*)`

하나 이상의 매개 변수를 지정된 값으로 설정합니다. 메서드 인수 구문은 URL 쿼리 문자열과 동일합니다. 즉, 와 구분된 이름=값 쌍을 나타냅니다 `&`. 쿼리 문자열, 이름 및 값과 동일한 값은 UTF8을 사용하여 퍼센트 인코딩됩니다. 호출하기 전에 `init()`로 지정하는 경우 이 매개 변수를 호출해야 합니다.

이 메서드는 뷰어 구성 정보가 `config` 생성자에 대한 JSON 개체.

참조 - [init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> params</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=값 매개 변수 쌍이 <span class="codeph"> &amp;</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 반환 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```css{.line-numbers}
<instance>.setParams("style=customStyle.css&VideoPlayer.playback=progressive")
```
