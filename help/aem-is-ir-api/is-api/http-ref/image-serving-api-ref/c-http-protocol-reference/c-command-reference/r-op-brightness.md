---
description: 밝기를 조정합니다. 이미지 밝기를 줄이거나 늘립니다.
solution: Experience Manager
title: op_brightness
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 390ed812-87ae-41e7-8021-65dd95915ae8
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 3%

---

# op_brightness{#op-brightness}

밝기를 조정합니다. 이미지 밝기를 줄이거나 늘립니다.

`op_brightness= *`adj`*`

<table id="simpletable_2B5DB95B1FF044C8BD226D4F8311E806"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>밝기 조정(-100..+100 int). </p></td> 
 </tr> 
</table>

## 속성 {#section-c7e757f63b2c4b5ebaacbadb51c72ce4}

레이어 명령. `layer=comp` 인 경우 현재 레이어 또는 복합 이미지에 적용됩니다. 효과 레이어에서 무시됨. 작업이 적용되기 전에 CMYK 이미지 또는 레이어가 RGB로 변환됩니다.

## 기본값 {#section-be56be0759634c79b4f264f194a94dbc}

`op_brightness=0`( 밝기 변경 없음)

## 예 {#section-c25f952f1b77409abb9ccf885862d75c}

전경 컨텐츠를 강조하기 위해 이미지의 배경을 약간 어둡게 합니다.

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_brightness=-10&layer=1&src=myRootId/myImageId`
