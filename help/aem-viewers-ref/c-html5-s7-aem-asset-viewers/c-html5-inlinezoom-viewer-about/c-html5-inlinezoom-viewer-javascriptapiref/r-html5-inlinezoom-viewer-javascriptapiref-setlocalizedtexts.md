---
description: 인라인 확대/축소 뷰어에 대한 JavaScript API 참조입니다.
seo-description: 인라인 확대/축소 뷰어에 대한 JavaScript API 참조입니다.
seo-title: setLocalizedText
solution: Experience Manager
title: setLocalizedText
topic: Dynamic media
uuid: 3e02e20f-2e81-4b4d-bf2a-cee8998faafb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setLocalizedText{#setlocalizedtexts}

인라인 확대/축소 뷰어에 대한 JavaScript API 참조입니다.

` setLocalizedTexts( *`localizationInfo`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 현지화 <span class="varname"> 정보 </span></span> </p> </td> 
   <td colname="col2"> <p> 현지화 데이터가 있는 { <span class="codeph"> } JSON </span>개체. </p> <p>자세한 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27" format="dita" scope="local"> 내용은 사용자 인터페이스 요소의 현지화를 </a> 참조하십시오. </p> <p>개체 <i>컨텐츠에 대한 자세한</i> 내용은 Viewer SDK 사용 안내서 및 예제를 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

하나 이상의 로케일에 대한 현지화 기호 값을 설정합니다. 이 매개 변수는 먼저 호출해야 합니다 `init()`.

또한 [init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6)를 참조하십시오.

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"FlyoutZoomView.TIP_BUBBLE_OVER":"Mouse over to zoom"},"fr":{"FlyoutZoomView.TIP_BUBBLE_OVER":"Passez la souris sur pour zoomer"},defaultLocale:"en"})
```

