---
description: 인라인 확대/축소 뷰어에 대한 JavaScript API 참조입니다.
seo-description: 인라인 확대/축소 뷰어에 대한 JavaScript API 참조입니다.
seo-title: setAsset
solution: Experience Manager
title: setAsset
topic: Dynamic media
uuid: 5bb7aebf-0a1d-4783-923d-7f7e7dcb9baa
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 2%

---


# setAsset{#setasset}

인라인 확대/축소 뷰어에 대한 JavaScript API 참조입니다.

` setAsset( *`asset`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 자산</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> 새 자산 ID, 명시적 이미지 세트 또는 프레임 특정 이미지 제공 수정자가 포함된 명시적 이미지 세트 및 명시적 이미지 세트. 선택 사항으로 <span class="codeph"> ?</span> 뒤에 글로벌 이미지 제공 수정자가 추가됩니다.</span> </p> <p> IR(이미지 렌더링) 또는 UGC(사용자 생성 콘텐츠)를 사용하는 이미지는 이 뷰어에서 지원되지 않습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

새 자산을 설정합니다. 이 매개 변수는 `init()` 이전 또는 이후에 언제든지 호출할 수 있습니다. `init()` 이후에 호출되는 경우 뷰어는 런타임에 에셋을 교환합니다.

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-init.md#reference-8651640683fc4a538bfb660709d1a463)도 참조하십시오.

## {#section-1d3cf85bc7cc4dfe9670e038d02b9101} 반환

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

프레임별 이미지 제공 수정자가 있는 명시적 이미지 세트:

```
<instance>.setAsset("(Scene7SharedAssets/Backpack_B?op_colorize=255%2C0%2C0,Scene7SharedAssets/Backpack_B?op_colorize=0x00ff00)")
```

선명하게 하기 수정자가 세트의 모든 이미지에 추가되었습니다.

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C?op_sharpen=1")
```

