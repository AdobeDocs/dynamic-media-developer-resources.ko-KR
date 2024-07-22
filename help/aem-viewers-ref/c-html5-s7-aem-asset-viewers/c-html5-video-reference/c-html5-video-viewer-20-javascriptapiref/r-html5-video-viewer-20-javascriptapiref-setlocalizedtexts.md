---
title: setLocalizedText
description: setLocalizedText
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 3bb1d277-e057-4a5d-9498-2adbca8f12b2
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 5%

---

# setLocalizedText{#setlocalizedtexts}

` setLocalizedTexts( *`localizationInfo`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo </span> </span> </p> </td> 
   <td colname="col2"> <p> 로컬라이제이션 데이터가 있는 { <span class="codeph"> 개체 </span>} JSON 개체입니다. </p> <p>자세한 내용은 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-namespace.md#concept-679bfabb3e3e4c12a285c4e9c4144153" format="dita" scope="local"> 뷰어 SDK 네임스페이스 </a>을(를) 참조하십시오. </p> <p>개체 콘텐츠에 대한 자세한 내용은 <i>Viewer SDK 사용 안내서</i>와 예제를 참조하십시오. 선택적. </p> </td> 
  </tr> 
 </tbody> 
</table>

하나 이상의 로케일에 대한 지역화 SYMBOL 값을 설정합니다. 이 매개 변수는 `init()` 전에 호출해야 합니다.

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6)도 참조하세요.

## 반환 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"VideoPlayer.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played."},"fr":{"VideoPlayer.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus."},defaultLocale:"en"})
```
