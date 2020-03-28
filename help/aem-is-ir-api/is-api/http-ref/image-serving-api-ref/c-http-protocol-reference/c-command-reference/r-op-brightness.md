---
description: 밝기 조정 이미지 밝기를 줄이거나 늘립니다.
seo-description: 밝기 조정 이미지 밝기를 줄이거나 늘립니다.
seo-title: op_brightness
solution: Experience Manager
title: op_brightness
topic: Scene7 Image Serving - Image Rendering API
uuid: 751ec9e5-4a70-438d-950c-deff4db034b1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# op_brightness{#op-brightness}

밝기 조정 이미지 밝기를 줄이거나 늘립니다.

`op_brightness= *`adj`*`

<table id="simpletable_2B5DB95B1FF044C8BD226D4F8311E806"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>명도 조정(-100...+100 int). </p></td> 
 </tr> 
</table>

## 속성 {#section-c7e757f63b2c4b5ebaacbadb51c72ce4}

레이어 명령. 현재 레이어 또는 합성 이미지에 적용됩니다( `layer=comp`경우). 효과 레이어에서 무시됩니다. CMYK 이미지 또는 레이어는 작업이 적용되기 전에 RGB로 변환됩니다.

## 기본값 {#section-be56be0759634c79b4f264f194a94dbc}

`op_brightness=0`을 클릭합니다.

## 예 {#section-c25f952f1b77409abb9ccf885862d75c}

이미지의 배경을 약간 어둡게 하여 전경 컨텐츠를 강조합니다.

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_brightness=-10&layer=1&src=myRootId/myImageId`
