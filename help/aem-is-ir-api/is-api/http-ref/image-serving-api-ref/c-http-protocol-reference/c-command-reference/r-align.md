---
title: 정렬
description: 보기에 맞게 이미지 정렬. 합성 이미지를 wid= 및 hei=로 정의된 보기 사각형 내에서 조정합니다(scl=도 지정된 경우 배율 조정 후 가능).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 01001cc6-1a60-4d6b-a27f-ea5822be6d11
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 1%

---

# 정렬{#align}

보기에 맞게 이미지 정렬. 합성 이미지를 wid= 및 hei=로 정의된 보기 사각형 내에서 조정합니다(scl=도 지정된 경우 배율 조정 후 가능).

` align= *`호리츠`*, *`세로`*`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 호리츠 </span> </span> </p> </td> 
  <td class="stentry"> <p>수평 정렬(실수, -1.0...1.0) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 세로 </span> </span> </p> </td> 
  <td class="stentry"> <p>수직 정렬(실수, -1.0...1.0) </p> </td> 
 </tr> 
</table>

지정 `align=-1,-1` 합성 이미지의 왼쪽 위를 뷰의 왼쪽 위와 정렬하려면 `align=1,1` 를 클릭하여 이미지의 오른쪽 하단과 보기의 오른쪽 하단을 맞춥니다. 표준 이미지 및 썸네일 요청의 경우, 합성 이미지 데이터로 가려지지 않는 보기의 모든 영역이 `bgc=`.

## 속성 {#section-3fbec8206fc944eda4746d8be84f3b41}

속성 보기. ( `align=` 워터마크 이미지와 워터마크가 적용되는 합성 이미지 간의 정렬을 정의하는 데에도 사용됩니다.) 현재 레이어 설정에 관계없이 적용됩니다. 다음 중 하나만 있는 경우 무시됨 `wid=` 및 `hei=` 은(는) 다음과 같은 경우에 지정됩니다. `fit=constrain` 또는 `fit=stretch`.

## 기본값 {#section-8a9ceff3dcc844c3af23b1c9066dac79}

`align=0,0`- 뷰 사각형에서 이미지를 가운데로 맞춥니다.

## 예 {#section-2c9447aa2e184fb8ab1a4370dc61d554}

다음 요청은 다음과 같습니다 `myImage` 를 200x200 픽셀 보기 사각형으로 바꿉니다.

`http://server/myRootId/myImageId?wid=200&hei=200&align=0,-1`

If `myImage` 는 정확히 정사각형이며 전체 보기 사각형을 채웁니다. If `myImage` 세로 종횡비가 있으며, 높이가 200픽셀이 되도록 크기가 조정되고 보기에서 가로로 가운데에 정렬됩니다. If `myImage` 가로 종횡비가 있으며 너비가 200픽셀로 조정되고 보기의 위쪽 가장자리에 정렬됩니다. 모든 경우에 반환되는 이미지는 크기가 정확히 200x200픽셀이며, 크기 조정으로 가려지지 않는 공간입니다 `myImage` 다음으로 채워짐: `attribute::BkgColor` (배경색을 동적으로 제어하려면 bgc=를 지정하십시오.)

## 참조 {#section-28b42c6db199456a800c8407faa26a99}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [맞춤=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), [워터마크](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-watermarks.md#reference-35d2c3a2c98349b792921c6cb8e73832)
