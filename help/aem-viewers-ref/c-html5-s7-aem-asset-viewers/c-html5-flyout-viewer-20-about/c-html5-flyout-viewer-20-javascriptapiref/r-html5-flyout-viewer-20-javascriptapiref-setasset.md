---
description: 플라이아웃 뷰어에 대한 JavaScript API 참조.
seo-description: 플라이아웃 뷰어에 대한 JavaScript API 참조.
seo-title: setAsset
solution: Experience Manager
title: setAsset
topic: Dynamic media
uuid: c6f7e7e9-084a-46ff-8cff-1ecb71f7b8d3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setAsset{#setasset}

플라이아웃 뷰어에 대한 JavaScript API 참조.

` setAsset( *`asset`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 자산</span></span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"></span>} 새로운 자산 ID, 명시적 이미지 세트 또는 프레임 특정 이미지 제공 한정자가 있는 명시적 이미지 세트, 선택적 글로벌 이미지 제공 수정자가 추가된 <span class="codeph"> ?</span>. </p> <p> IR(이미지 렌더링) 또는 UGC(사용자 생성 컨텐츠)를 사용하는 이미지는 이 뷰어에서 지원되지 않습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

새 자산을 설정합니다. 이 매개 변수는 그 전후에 언제든지 호출할 수 `init()`있습니다. 이후에 호출되면 뷰어는 런타임 시 자산을 `init()`교체합니다.

또한 [init](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-init.md#reference-8651640683fc4a538bfb660709d1a463)를 참조하십시오.

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

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

