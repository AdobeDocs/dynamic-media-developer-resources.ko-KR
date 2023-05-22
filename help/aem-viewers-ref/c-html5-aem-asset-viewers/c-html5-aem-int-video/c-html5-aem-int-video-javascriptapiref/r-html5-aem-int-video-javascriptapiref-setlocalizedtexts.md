---
title: setLocalizedText
description: 대화형 비디오 뷰어에 대한 JavaScript API 참조입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 2fd557ad-088a-4ddc-8c00-b3cf3d2d9a2f
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 2%

---

# setLocalizedText{#setlocalizedtexts}

대화형 비디오 뷰어에 대한 JavaScript API 참조입니다.

` setLocalizedTexts( *`localizationInfo`*)`

하나 이상의 로케일에 대한 지역화 SYMBOL 값을 설정합니다. 이 매개 변수는 다음 전에 호출해야 합니다. `init()`.

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo </span> </span> </p> </td> 
   <td colname="col2"> <p> { <span class="codeph"> 오브젝트 </span>현지화 데이터가 있는 } JSON 개체. </p> <p>다음을 참조하십시오 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> 사용자 인터페이스 요소의 현지화 </a> 추가 정보. </p> <p>다음 항목도 참조하십시오. <i>Viewer SDK 사용 안내서</i> 객체의 컨텐트에 대한 자세한 내용은 예제를 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

참조: [init](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## 반환 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"VideoPlayer.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played."},"fr":{"VideoPlayer.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus."},defaultLocale:"en"})
```
