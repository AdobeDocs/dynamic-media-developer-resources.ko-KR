---
description: 혼합 미디어 뷰어에 대한 JavaScript API 참조입니다.
seo-description: 혼합 미디어 뷰어에 대한 JavaScript API 참조입니다.
seo-title: setLocalizedText
solution: Experience Manager
title: setLocalizedText
uuid: 86e2e70e-2147-4e63-9204-7a7a8566c3e6
feature: Dynamic Media Classic,뷰어,SDK/API,혼합 미디어 집합
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 2%

---


# setLocalizedText{#setlocalizedtexts}

혼합 미디어 뷰어에 대한 JavaScript API 참조입니다.

` setLocalizedTexts( *`localizationInfo`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo</span> </span> </p> </td> 
   <td colname="col2"> <p> 현지화 데이터가 포함된 JSON 개체 {<span class="codeph"></span>} </p> <p>자세한 내용은 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1" format="dita" scope="local"> 사용자 인터페이스 요소</a>의 현지화를 참조하십시오. </p> <p>개체 내용에 대한 자세한 내용은 <i>뷰어 SDK 사용자 안내서</i> 및 예제를 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

하나 이상의 로캘에 대한 현지화 기호 값을 설정합니다. 이 매개 변수는 `init()` 이전에 호출해야 합니다.

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae)도 참조하십시오.

## {#section-1d3cf85bc7cc4dfe9670e038d02b9101} 반환

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"CloseButton.TOOLTIP":"Close"},"fr":{"CloseButton.TOOLTIP":"Fermer"},defaultLocale:"en"})
```

