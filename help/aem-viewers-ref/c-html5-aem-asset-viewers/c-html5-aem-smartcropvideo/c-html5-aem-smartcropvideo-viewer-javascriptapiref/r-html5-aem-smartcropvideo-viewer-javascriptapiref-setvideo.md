---
title: setVideo
description: 스마트 자르기 비디오 뷰어에 대한 JavaScript API 참조
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 5e735e11-e359-4b98-b4a9-2c69a8eb424a
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 2%

---

# setVideo{#setvideo}

스마트 자르기 비디오 뷰어에 대한 JavaScript API 참조

`setVideo(videoUrl[, data])`

새 외부 비디오 및 선택적 추가 비디오 데이터를 설정합니다. 전후에 언제든지 호출할 수 있습니다. `init()`. 다음 시간 이후에 호출되는 경우 `init()`, 뷰어가 런타임에 비디오를 교체합니다.

참조: [init]
(../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6).

## 매개 변수 {#section-b6affc90b3a84584b684641c86862e01}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> videoUrl </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> 문자열 </span>새 비디오의 절대 URL입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 데이터 </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> JSON </span>다음 선택 필드가 있는 } JSON 개체(대/소문자 구분): </p> <p> 
     <ul id="ul_26121393BC7145FF8A43C05ACCBEFF36"> 
      <li id="li_DA50E073F3D4460CBC34243A2CBCC895"> <span class="codeph"> 후기 </span> - 비디오 재생이 시작되기 전에 첫 번째 프레임에 표시할 이미지입니다. 다음을 참조하십시오 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-cmdref/r-html5-video-viewer-conf-attrib-videoplayer-posterimage.md#reference-9739abeeb9f64c02b5d2f7a0d1706103" format="dita" scope="local"> VideoPlayer.posterimage </a>. </li> 
      <li id="li_4659E82D38EB4438AAA04FDEAF21B087"> <span class="codeph"> 캡션 </span> - 새 캡션 파일의 위치입니다. 캡션 파일을 지정하지 않으면 캡션 단추가 사용자 인터페이스에 표시되지 않습니다. </li> 
      <li id="li_A43A1BAB6B0F4A7981F71408F08F07D1"> <span class="codeph"> 탐색 </span> - WebVTT 탐색 컨텐츠의 URL 또는 경로입니다. WebVTT 파일은 이미지 제공에 의해 제공되어야 합니다. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 반환 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setVideo("https://s7d9.scene7.com/is/content/Scene7SharedAssets/Glacier_Climber_MP4")
```
