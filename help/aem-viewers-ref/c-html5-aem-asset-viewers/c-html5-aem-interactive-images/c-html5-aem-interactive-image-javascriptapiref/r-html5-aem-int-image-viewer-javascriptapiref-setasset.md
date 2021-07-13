---
description: 비디오 이미지 뷰어에 대한 JavaScript API 참조.
solution: Experience Manager
title: setAsset
feature: Dynamic Media Classic,Viewers,SDK/API,대화형 이미지
role: Developer,User
exl-id: e5f88bc9-a880-45eb-9554-57e185937d29
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 3%

---

# setAsset{#setasset}

비디오 이미지 뷰어에 대한 JavaScript API 참조.

` setAsset( *`asset`*)`

새 자산을 설정합니다. 이 매개 변수는 `init()` 전이나 후에 언제든지 호출할 수 있습니다. `init()` 다음에 호출되면 뷰어는 런타임 시 자산을 교체합니다.

[init](../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-javascriptapiref/r-html5-aem-int-image-viewer-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)도 참조하십시오.

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 자산</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> 문자열</span>}의 새 자산 ID입니다. </p> <p>IR(이미지 렌더링) 또는 UGC(사용자 생성 컨텐츠)를 사용하는 이미지는 이 뷰어에서 지원되지 않습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 반환 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

단일 이미지 참조:

```
<instance>.setAsset("/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg")
```
