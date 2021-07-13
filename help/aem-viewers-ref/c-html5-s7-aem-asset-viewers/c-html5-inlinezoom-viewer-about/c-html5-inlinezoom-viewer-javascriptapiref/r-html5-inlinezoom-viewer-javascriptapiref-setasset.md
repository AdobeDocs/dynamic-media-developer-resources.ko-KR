---
description: 인라인 확대/축소 뷰어에 대한 JavaScript API 참조.
solution: Experience Manager
title: setAsset
feature: Dynamic Media Classic,Viewers,SDK/API,인라인 확대/축소
role: Developer,User
exl-id: 62b46ad5-90b7-49e1-a426-87fbe956f07e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 2%

---

# setAsset{#setasset}

인라인 확대/축소 뷰어에 대한 JavaScript API 참조.

` setAsset( *`asset`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 자산</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> String</span>}에 새로운 자산 id, 명시적 이미지 세트 또는 프레임 특정 이미지 제공 한정자가 포함된 명시적 이미지 세트, <span class="codeph"> ?</span> 뒤에 글로벌 이미지 제공 한정자를 추가할 수 있습니다. </p> <p> IR(이미지 렌더링) 또는 UGC(사용자 생성 콘텐츠)를 사용하는 이미지는 이 뷰어에서 지원되지 않습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

새 자산을 설정합니다. 이 매개 변수는 `init()` 전이나 후에 언제든지 호출할 수 있습니다. `init()` 다음에 호출되면 뷰어는 런타임 시 자산을 교체합니다.

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-init.md#reference-8651640683fc4a538bfb660709d1a463)도 참조하십시오.

## 반환 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

단일 이미지 참조:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B")
```

카탈로그에 정의된 이미지 세트에 대한 단일 참조:

```
<instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample")
```

명시적 이미지 세트:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C")
```

프레임별 이미지 제공 한정자를 사용한 명시적 이미지 세트:

```
<instance>.setAsset("(Scene7SharedAssets/Backpack_B?op_colorize=255%2C0%2C0,Scene7SharedAssets/Backpack_B?op_colorize=0x00ff00)")
```

선명하게 하기 수정자가 세트의 모든 이미지에 추가되었습니다.

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C?op_sharpen=1")
```
