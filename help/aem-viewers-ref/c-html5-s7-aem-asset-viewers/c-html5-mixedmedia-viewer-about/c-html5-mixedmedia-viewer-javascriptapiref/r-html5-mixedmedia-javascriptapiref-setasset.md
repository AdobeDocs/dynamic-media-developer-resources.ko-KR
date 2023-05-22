---
title: setAsset
description: 혼합 미디어 뷰어에 대한 JavaScript API 참조입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 3ad78de9-17a6-40c9-b389-a1f7eed11635
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 1%

---

# setAsset{#setasset}

혼합 미디어 뷰어에 대한 JavaScript API 참조입니다.

` setAsset( *`asset`*[,data]))`

새 에셋과 선택적 추가 에셋 데이터를 설정합니다. 이 매개 변수는 언제든지 전후에 호출할 수 있습니다 `init()`. 다음 시간 이후에 호출되는 경우 `init()`, 뷰어는 런타임 시 자산을 교체합니다.

참조: [init](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae).

## 매개 변수 {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

`*`자산`*` - { `String`} 새 자산 ID 또는 명시적 혼합 미디어 집합으로, 뒤에 선택적 이미지 제공 수정자가 추가됨 `?`.

IR(이미지 렌더링) 또는 UGC(사용자 생성 컨텐츠)를 사용하는 이미지는 이 뷰어에서 지원되지 않습니다.

`*`데이터`*` - { `JSON`} 새 캡션 파일의 위치입니다.

지정하지 않으면 캡션 단추가 사용자 인터페이스에 표시되지 않습니다. 이 매개 변수로 지정된 캡션은 혼합 미디어 집합에서 먼저 제공되는 비디오에 적용됩니다. 이후 비디오는 캡션 없이 재생됩니다. 이 뷰어는 다음 구성 요소 ID를 지원합니다.

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>구성 요소 ID </p> </th> 
   <th colname="col2" class="entry"> <p>Viewer SDK 구성 요소 클래스 이름 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 후기 </span> </p> </td> 
   <td colname="col2"> <p>비디오 재생이 시작되기 전에 첫 번째 프레임에 표시할 이미지입니다. </p> <p>다음을 참조하십시오 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-posterimage.md#reference-f424ad0f278b4d14b86ea55e3a73c52b" format="dita" scope="local"> VideoPlayer.posterimage </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 캡션 </span> </p> </td> 
   <td colname="col2"> <p> 새 캡션 파일의 위치입니다. </p> <p>지정하지 않으면 캡션 단추가 사용자 인터페이스에 표시되지 않습니다. 이 매개 변수로 지정된 캡션은 미디어 세트에서 맨 처음 나오는 비디오에 적용됩니다. 후속 비디오는 캡션 없이 재생됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 반환 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

단일 미디어 세트 참조:

```
<instance>.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample")
```

명시적 미디어 집합:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_J;;advanced_image;,Scene7SharedAssets/Frame-6;;advanced_image;,Scene7SharedAssets/Frame-2;;advanced_image;,Scene7SharedAssets/SpinSet_Sample;;spin;,Scene7SharedAssets/ImageSet-Colors-Sample;;advanced_swatchset;,Scene7SharedAssets/Glacier_Climber_640x360;Scene7SharedAssets/Glacier_Climber_640x360;video;")
```

선명하게 하기 수정자가 세트의 모든 이미지에 추가되었습니다.

```
<instance>.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample?op_sharpen=1")
```
