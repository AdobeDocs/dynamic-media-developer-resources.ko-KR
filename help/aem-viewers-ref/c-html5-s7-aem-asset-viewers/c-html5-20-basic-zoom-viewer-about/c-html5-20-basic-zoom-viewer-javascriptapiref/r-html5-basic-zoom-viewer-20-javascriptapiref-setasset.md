---
description: 기본 확대/축소 뷰어용 JavaScript API 참조.
seo-description: 기본 확대/축소 뷰어용 JavaScript API 참조.
seo-title: setAsset
solution: Experience Manager
title: setAsset
uuid: af433f15-34a0-4867-97c5-acab47e3e008
feature: Dynamic Media Classic,뷰어,SDK/API,확대/축소
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 2%

---


# setAsset{#setasset}

기본 확대/축소 뷰어용 JavaScript API 참조.

` setAsset( *`asset`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 자산</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> 문자열</span>} 새 자산 ID와 옵션 IS 수정자가 "?" 다음에 추가됩니다. </p> <p> IR(이미지 렌더링) 또는 UGC(사용자 생성 콘텐츠)를 사용하는 이미지는 이 뷰어에서 지원되지 않습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

새 자산을 설정합니다. 이 매개 변수는 `init()` 이전 또는 이후에 언제든지 호출할 수 있습니다. `init()` 이후에 호출되는 경우 뷰어는 런타임에 에셋을 교환합니다.

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-javascriptapiref/r-html5-basic-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)도 참조하십시오.

## {#section-1d3cf85bc7cc4dfe9670e038d02b9101} 반환

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

단일 이미지 참조:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B")
```

선명하게 하기 수정자가 세트의 모든 이미지에 추가되었습니다.

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B?op_sharpen=1")
```

