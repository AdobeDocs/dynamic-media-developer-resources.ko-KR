---
description: 비디오 뷰어용 JavaScript API 참조
seo-description: 비디오 뷰어용 JavaScript API 참조
seo-title: setVideo
solution: Experience Manager
title: setVideo
topic: Dynamic media
uuid: 0a1b3caa-ded6-4020-962c-41c3ece0a865
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 3%

---


# setVideo{#setvideo}

비디오 뷰어용 JavaScript API 참조

`setVideo(videoUrl[, data])`

새 외부 비디오 및 선택적 추가 비디오 데이터를 설정합니다. `init()` 전후에 언제든지 호출할 수 있습니다. `init()` 이후에 호출되는 경우 뷰어는 런타임에 비디오를 교환합니다.

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6)도 참조하십시오.

## 매개 변수 {#section-b6affc90b3a84584b684641c86862e01}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> videoUrl  </span> </p> </td> 
   <td colname="col2"> <p>새 비디오에 대한 절대 URL을 <span class="codeph"> 문자열 </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 데이터 </span> </p> </td> 
   <td colname="col2"> <p>다음 선택적 필드가 있는 { <span class="codeph"> JSON </span>} JSON 개체(대/소문자 구분): </p> <p> 
     <ul id="ul_26121393BC7145FF8A43C05ACCBEFF36"> 
      <li id="li_DA50E073F3D4460CBC34243A2CBCC895"> <span class="codeph"> 포스터 이미지  </span> - 비디오 재생이 시작되기 전에 첫 번째 프레임에 표시할 이미지입니다. <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-cmdref/r-html5-video-viewer-conf-attrib-videoplayer-posterimage.md#reference-9739abeeb9f64c02b5d2f7a0d1706103" format="dita" scope="local"> VideoPlayer.포스터 이미지 </a>를 참조하십시오. </li> 
      <li id="li_4659E82D38EB4438AAA04FDEAF21B087"> <span class="codeph"> 캡션  </span> - 새 캡션 파일의 위치입니다. 캡션 파일을 지정하지 않으면 캡션 단추가 사용자 인터페이스에 표시되지 않습니다. </li> 
      <li id="li_A43A1BAB6B0F4A7981F71408F08F07D1"> <span class="codeph"> 탐색  </span> - WebVTT 탐색 컨텐츠의 URL 또는 경로 WebVTT 파일은 이미지 제공에서 제공해야 합니다. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## {#section-1d3cf85bc7cc4dfe9670e038d02b9101} 반환

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setVideo("https://s7d9.scene7.com/is/content/Scene7SharedAssets/Glacier_Climber_MP4")
```

