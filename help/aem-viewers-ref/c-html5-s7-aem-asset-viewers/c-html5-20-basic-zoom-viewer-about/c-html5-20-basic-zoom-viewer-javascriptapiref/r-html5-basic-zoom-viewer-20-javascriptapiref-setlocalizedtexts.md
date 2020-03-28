---
description: 기본 확대/축소 뷰어용 JavaScript API 참조.
seo-description: 기본 확대/축소 뷰어용 JavaScript API 참조.
seo-title: setLocalizedText
solution: Experience Manager
title: setLocalizedText
topic: Dynamic media
uuid: 34a2ea4e-5493-41fa-92bf-5cebe66f6370
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setLocalizedText{#setlocalizedtexts}

기본 확대/축소 뷰어용 JavaScript API 참조.

` setLocalizedTexts( *`localizationInfo`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 현지화 <span class="varname"> 정보</span></span> </p> </td> 
   <td colname="col2"> <p> 현지화<span class="codeph"> 데이터가 있는 {</span>} JSON 개체. </p> <p>자세한 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> 내용은 사용자 인터페이스 요소의</a> 현지화를 참조하십시오. </p> <p> 개체 <i>컨텐츠에 대한 자세한</i> 내용은 Viewer SDK 사용 안내서 및 예제를 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

하나 이상의 로케일에 대한 현지화 기호 값을 설정합니다. 이 매개 변수는 먼저 호출해야 합니다 `init()`.

또한 [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-javascriptapiref/r-html5-basic-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)를 참조하십시오.

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"CloseButton.TOOLTIP":"Close"},"fr":{"CloseButton.TOOLTIP":"Fermer"},defaultLocale:"en"})
```

