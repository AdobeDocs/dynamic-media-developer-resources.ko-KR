---
description: 회전판 뷰어에 대한 JavaScript API 참조.
seo-description: 회전판 뷰어에 대한 JavaScript API 참조.
seo-title: setAsset
solution: Experience Manager
title: setAsset
topic: Dynamic media
uuid: 770cbb87-af86-48dc-88a0-e74f6716f545
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setAsset{#setasset}

회전판 뷰어에 대한 JavaScript API 참조.

` setAsset( *`asset`*)`

새 자산을 설정합니다. 이 매개 변수는 그 전후에 언제든지 호출할 수 `init()`있습니다. 이후에 호출되면 뷰어는 런타임 시 자산을 `init()`교체합니다.

또한 [init](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)를 참조하십시오.

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 자산</span></span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> String</span>} 새 자산 ID. </p> <p>IR(이미지 렌더링) 또는 UGC(사용자 생성 컨텐츠)를 사용하는 이미지는 이 뷰어에서 지원되지 않습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

단일 이미지 참조:

```
<instance>.setAsset("/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner")
```

