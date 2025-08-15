---
description: 비디오 뷰어에 대한 JavaScript API 참조.
solution: Experience Manager
title: setLocalizedText
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: dfd57bde-70cd-483f-bcd4-680186e4a733
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 2%

---

# setLocalizedText{#setlocalizedtexts}

비디오 뷰어에 대한 JavaScript API 참조.

[!DNL ` setLocalizedTexts( *`localizationInfo`*)`]

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo</span> </span> </p> </td> 
   <td colname="col2"> <p> 로컬라이제이션 데이터가 있는 {<span class="codeph"> 개체</span>} JSON 개체입니다. </p> <p>자세한 내용은 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> 사용자 인터페이스 요소의 지역화</a>을(를) 참조하십시오. </p> <p>개체 콘텐츠에 대한 자세한 내용은 <i>Viewer SDK 사용 안내서</i> 및 예제를 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

하나 이상의 로케일에 대한 지역화 SYMBOL 값을 설정합니다. 이 매개 변수는 [!DNL `init()`] 전에 호출해야 합니다.

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)도 참조하세요.

## 반환 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"CloseButton.TOOLTIP":"Close"},"fr":{"CloseButton.TOOLTIP":"Fermer"},defaultLocale:"en"})
```
