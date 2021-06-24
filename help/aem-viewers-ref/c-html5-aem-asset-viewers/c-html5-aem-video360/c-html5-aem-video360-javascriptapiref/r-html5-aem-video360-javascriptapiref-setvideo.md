---
description: Video360 뷰어에 대한 JavaScript API 참조
solution: Experience Manager
title: setVideo
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR 비디오
role: Developer,Business Practitioner
exl-id: e1894d96-6f37-4e34-a709-5b0121bd0696
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 4%

---

# setVideo{#setvideo}

Video360 뷰어에 대한 JavaScript API 참조

`setVideo(videoUrl)`

새 외부 비디오를 설정합니다. `init()` 이전 및 이후에 언제든지 호출할 수 있습니다. `init()` 다음에 를 호출하면 뷰어는 런타임 시 비디오를 교체합니다.

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6)도 참조하십시오.

## 매개 변수 {#section-b6affc90b3a84584b684641c86862e01}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> videoUrl  </span> </p> </td> 
   <td colname="col2"> <p>새 비디오에 대한 절대 URL을 {<span class="codeph"> 문자열</span>} . </p> </td> 
  </tr> 
 </tbody> 
</table>

## 반환 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setVideo("https://s7d9.scene7.com/is/content/Viewers/space_station_360")
```
