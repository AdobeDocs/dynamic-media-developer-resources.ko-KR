---
title: setAsset
description: 비디오 뷰어에 대한 JavaScript API 참조.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 4fc94f30-e330-4c8a-b6da-d870e4f8e4ab
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 1%

---

# setAsset{#setasset}

비디오 뷰어에 대한 JavaScript API 참조.

` setAsset( *`자산`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 자산 </span> </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> 문자열 </span>} 새 자산 id, 명시적 이미지 집합 또는 프레임별 이미지 제공 수정자를 사용하는 명시적 이미지 집합이며, 선택적 전역 이미지 제공 수정자는 "?" 뒤에 추가됩니다. </p> <p> IR(이미지 렌더링) 또는 UGC(사용자 생성 컨텐츠)를 사용하는 이미지는 이 뷰어에서 지원되지 않습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

새 자산을 설정합니다. 이 매개 변수는 `init()` 전이나 후에 언제든지 호출할 수 있습니다. `init()` 이후에 호출되는 경우 뷰어는 런타임 시 자산을 교체합니다.

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)도 참조하세요.

## 반환 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

다음과 같은 단일 이미지 참조:

```
 <instance>.setAsset("Scene7SharedAssets/Backpack_B")
```

카탈로그에 정의된 이미지 세트에 대한 단일 참조는 다음과 같습니다.

```
 <instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample")
```

명시적 이미지 집합은 다음과 같습니다.

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C")
```

다음과 같이 프레임별 이미지 제공 수정자를 사용하는 명시적 이미지 집합입니다.

```
 <instance>.setAsset("(Scene7SharedAssets/Backpack_B?op_colorize=255%2C0%2C0,Scene7SharedAssets/Backpack_B?op_colorize=0x00ff00)")
```

선명하게 하기 수정자는 다음과 같이 세트의 모든 이미지에 추가되었습니다.

```
 <instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample?op_sharpen=1")
```
