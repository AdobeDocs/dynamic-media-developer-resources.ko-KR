---
description: 회전판 뷰어에 대한 JavaScript API 참조입니다.
seo-description: 회전판 뷰어에 대한 JavaScript API 참조입니다.
seo-title: setLocalizedText
solution: Experience Manager
title: setLocalizedText
topic: Dynamic media
uuid: f69d3232-dd7c-41b5-87a0-146b8fb1bdb1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 2%

---


# setLocalizedText{#setlocalizedtexts}

회전판 뷰어에 대한 JavaScript API 참조입니다.

` setLocalizedTexts( *`localizationInfo`*)`

하나 이상의 로캘에 대한 현지화 기호 값을 설정합니다. 이 매개 변수는 `init()` 이전에 호출해야 합니다.

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo</span> </span> </p> </td> 
   <td colname="col2"> <p> 현지화 데이터가 포함된 JSON 개체 {<span class="codeph"></span>} </p> <p>자세한 내용은 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-localization.md" format="dita" scope="local"> 사용자 인터페이스 요소</a>의 현지화를 참조하십시오. </p> <p>개체 내용에 대한 자세한 내용은 <i>뷰어 SDK 사용자 안내서</i> 및 예제를 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

[init](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)도 참조하십시오.

## {#section-1d3cf85bc7cc4dfe9670e038d02b9101} 반환

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"PanLeftButton.TOOLTIP":"Left"},"fr":{"PanLeftButton.TOOLTIP":"Gauchiste"},defaultLocale:"en"})
```

