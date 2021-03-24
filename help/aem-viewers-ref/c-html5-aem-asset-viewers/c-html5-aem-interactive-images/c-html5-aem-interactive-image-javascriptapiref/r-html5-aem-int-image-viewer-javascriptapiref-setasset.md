---
description: 비디오 이미지 뷰어용 JavaScript API 참조.
solution: Experience Manager
title: setAsset
feature: Dynamic Media Classic,뷰어,SDK/API,대화형 이미지
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 3%

---


# setAsset{#setasset}

비디오 이미지 뷰어용 JavaScript API 참조.

` setAsset( *`asset`*)`

새 자산을 설정합니다. 이 매개 변수는 `init()` 이전 또는 이후에 언제든지 호출할 수 있습니다. `init()` 이후에 호출되는 경우 뷰어는 런타임에 에셋을 교환합니다.

[init](../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-javascriptapiref/r-html5-aem-int-image-viewer-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)도 참조하십시오.

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 자산</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> 새 자산 ID 문자열</span>} </p> <p>IR(이미지 렌더링) 또는 UGC(사용자 생성 콘텐츠는 이 뷰어에서 지원되지 않습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## {#section-1d3cf85bc7cc4dfe9670e038d02b9101} 반환

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

단일 이미지 참조:

```
<instance>.setAsset("/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg")
```

