---
title: setAsset
description: 스마트 자르기 비디오 뷰어에 대한 JavaScript API 참조.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: e5d71393-fcae-4bd4-8e78-a451b2f05ffc
source-git-commit: b6ebc938f55117c4144ff921bed7f8742cf3a8a7
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 3%

---

# setAsset{#setasset}

스마트 자르기 비디오 뷰어에 대한 JavaScript API 참조.

`setAsset(asset[, data])`

새 자산 및 선택적 추가 자산 데이터를 설정합니다. 이 매개 변수는 이전 또는 이후에 언제든지 호출할 수 있습니다 `init()`. 호출 후에 `init()`로 설정하면 뷰어가 런타임 시 자산을 교체합니다.

참조 - [init]
(.../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref\r-html5-aem-smartcropvideo-viewer-javascripdiref-init.md#reference-3b570ba8b35045.md6b30fb178c21a66c6).

## 매개 변수 {#section-e030b401b966469cb5dd121501161c2a}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> asset </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> 문자열 </span>} 새 자산 ID를 반환합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 데이터 </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> JSON </span>} 선택적 필드(대/소문자 구분)가 있는 JSON 개체. </p> <p> 
     <ul id="ul_26121393BC7145FF8A43C05ACCBEFF36"> 
      <li id="li_DA50E073F3D4460CBC34243A2CBCC895"> <span class="codeph"> 포스터이미지 </span> - 비디오가 재생을 시작하기 전에 첫 번째 프레임에 표시할 이미지입니다. 자세한 내용은 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-cmdref/r-html5-aem-smartcropvideo-conf-attrib-videoplayer-posterimage.md#reference-9739abeeb9f64c02b5d2f7a0d1706103" format="dita" scope="local"> VideoPlayer.posterimage </a>. </li> 
      <li id="li_BBFF3965B69A4AC8A469FDB69097B25A"> <span class="codeph"> 캡션 </span> - 새 닫힌 캡션 파일의 위치. 파일을 지정하지 않으면 사용자 인터페이스에 닫힌 캡션 단추가 표시되지 않습니다. </li> 
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
