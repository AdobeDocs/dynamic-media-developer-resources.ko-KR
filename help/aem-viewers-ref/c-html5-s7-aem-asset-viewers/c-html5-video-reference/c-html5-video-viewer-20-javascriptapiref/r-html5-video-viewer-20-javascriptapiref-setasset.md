---
title: setAsset
description: 비디오 뷰어에 대한 JavaScript API 참조.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: e5d71393-fcae-4bd4-8e78-a451b2f05ffc
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 2%

---

# setAsset{#setasset}

비디오 뷰어에 대한 JavaScript API 참조.

`setAsset(asset[, data])`

새 에셋과 선택적 추가 에셋 데이터를 설정합니다. 이 매개 변수는 `init()` 전이나 후에 언제든지 호출할 수 있습니다. `init()` 이후에 호출되는 경우 뷰어는 런타임 시 자산을 교체합니다.

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6)도 참조하세요.

## 매개 변수 {#section-e030b401b966469cb5dd121501161c2a}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 자산 </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> 문자열 </span>} 새 자산 ID입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 데이터 </span> </p> </td> 
   <td colname="col2"> <p>다음 선택적 필드가 포함된 { <span class="codeph"> JSON </span>} JSON 개체(대/소문자 구분): </p> <p> 
     <ul id="ul_26121393BC7145FF8A43C05ACCBEFF36"> 
      <li id="li_DA50E073F3D4460CBC34243A2CBCC895"> <span class="codeph"> 포스터이미지 </span> - 비디오 재생이 시작되기 전에 첫 번째 프레임에 표시할 이미지입니다. <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-cmdref/r-html5-video-viewer-conf-attrib-videoplayer-posterimage.md#reference-9739abeeb9f64c02b5d2f7a0d1706103" format="dita" scope="local"> VideoPlayer.posterimage </a>을(를) 참조하십시오. </li> 
      <li id="li_BBFF3965B69A4AC8A469FDB69097B25A"> <span class="codeph"> 캡션 </span> - 새 폐쇄 캡션 파일의 위치입니다. 파일을 지정하지 않으면 사용자 인터페이스에 닫힌 캡션 단추가 표시되지 않습니다. </li> 
      <li id="li_4659E82D38EB4438AAA04FDEAF21B087"> <span class="codeph"> 탐색 </span> - WebVTT 탐색 컨텐츠의 URL 또는 경로입니다. WebVTT 파일은 이미지 제공에 의해 제공되어야 합니다. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 반환 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setAsset("Scene7SharedAssets/Glacier_Climber_MP4")
```
