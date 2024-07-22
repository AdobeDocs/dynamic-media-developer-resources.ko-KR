---
title: setAsset
description: 대화형 비디오 뷰어에 대한 JavaScript API 참조입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 24d8d11d-4688-4ca0-92ae-824a5e984a10
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 1%

---

# setAsset{#setasset}

대화형 비디오 뷰어에 대한 JavaScript API 참조입니다.

`setAsset(asset[, data])`

새 에셋과 선택적 추가 에셋 데이터를 설정합니다. 이 매개 변수는 `init()` 전이나 후에 언제든지 호출할 수 있습니다. `init()` 이후에 호출되는 경우 뷰어는 런타임 시 자산을 교체합니다.

[init](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)도 참조하세요.

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 자산 </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> 문자열 </span>} 새 자산 ID입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 데이터 </span> </p> </td> 
   <td colname="col2"> <p> 다음 선택적 필드가 포함된 { <span class="codeph"> JSON </span>} JSON 개체(대/소문자 구분): </p> <p> 
     <ul id="ul_924FB99ACF0F43699CD229593F1C1384"> 
      <li id="li_F3CFEF28BCB7450991EFE0BD4EB28E36"> <span class="codeph"> 포스터이미지 </span> - 비디오 재생이 시작되기 전에 첫 번째 프레임에 표시할 이미지입니다. <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/r-html5-aem-int-video-config-attrib/r-html5-aem-int-video-config-attrib-videoplayer-posterimage.md#reference-8e8e2b3e7e9c4ee8b6dadf90cef494f7" format="dita" scope="local"> VideoPlayer.posterimage </a>을(를) 참조하십시오. </li> 
      <li id="li_D6C3E543C70942C582020780E2DF74C8"> <span class="codeph"> 캡션 </span> - 새 캡션 파일의 위치입니다. 지정하지 않으면 캡션 단추가 사용자 인터페이스에 표시되지 않습니다. </li> 
      <li id="li_BF866BD7275E450EA08A0E72FAA9D3AE"> <span class="codeph"> 탐색 </span> - WebVTT 탐색 컨텐츠의 URL 또는 경로입니다. WebVTT 파일은 이미지 제공에 의해 제공되어야 합니다. </li> 
      <li id="li_0C0EC5AB00554EC6AA01F60684A40213"> <span class="codeph"> interactiveData </span> - WebVTT 대화형 데이터 콘텐츠의 URL 또는 경로입니다. WebVTT 파일은 이미지 제공에 의해 제공되어야 합니다. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 반환 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setAsset("/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4")
```
