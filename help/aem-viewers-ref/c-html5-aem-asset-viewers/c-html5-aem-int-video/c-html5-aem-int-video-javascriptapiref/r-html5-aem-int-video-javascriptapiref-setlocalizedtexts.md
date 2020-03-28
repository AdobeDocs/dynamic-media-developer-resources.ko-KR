---
description: 대화형 비디오 뷰어용 JavaScript API 참조.
seo-description: 대화형 비디오 뷰어용 JavaScript API 참조.
seo-title: setLocalizedText
solution: Experience Manager
title: setLocalizedText
topic: Dynamic media
uuid: 11844a71-adb0-42a9-9b58-b69821070fd2
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# setLocalizedText{#setlocalizedtexts}

대화형 비디오 뷰어용 JavaScript API 참조.

` setLocalizedTexts( *`localizationInfo`*)`

하나 이상의 로케일에 대한 현지화 기호 값을 설정합니다. 이 매개 변수는 먼저 호출해야 합니다 `init()`.

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 현지화 <span class="varname"> 정보 </span></span> </p> </td> 
   <td colname="col2"> <p> 현지화 데이터가 있는 { <span class="codeph"> } JSON </span>개체. </p> <p>자세한 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> 내용은 사용자 인터페이스 요소의 현지화를 </a> 참조하십시오. </p> <p>개체 <i>컨텐츠에 대한 자세한</i> 내용은 Viewer SDK 사용 안내서 및 예제를 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

또한 [init](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)를 참조하십시오.

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"VideoPlayer.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played."},"fr":{"VideoPlayer.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus."},defaultLocale:"en"})
```

