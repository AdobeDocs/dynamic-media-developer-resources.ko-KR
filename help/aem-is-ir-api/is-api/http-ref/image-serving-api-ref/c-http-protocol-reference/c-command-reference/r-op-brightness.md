---
title: op_brightness
description: 밝기를 조정합니다. 이미지 밝기를 줄이거나 늘립니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 390ed812-87ae-41e7-8021-65dd95915ae8
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 2%

---

# op_brightness{#op-brightness}

밝기를 조정합니다. 이미지 밝기를 줄이거나 늘립니다.

`op_brightness= *`adj`*`

<table id="simpletable_2B5DB95B1FF044C8BD226D4F8311E806"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>밝기 조정(-100...+100int). </p></td> 
 </tr> 
</table>

## 속성 {#section-c7e757f63b2c4b5ebaacbadb51c72ce4}

레이어 명령. 다음과 같은 경우 현재 레이어 또는 합성 이미지에 적용됩니다. `layer=comp`. 효과 레이어에서 무시됨. CMYK 이미지 또는 레이어는 작업을 적용하기 전에 RGB으로 변환됩니다.

## 기본값 {#section-be56be0759634c79b4f264f194a94dbc}

`op_brightness=0`을 참조하십시오.

## 예 {#section-c25f952f1b77409abb9ccf885862d75c}

이미지의 배경을 약간 어둡게 하여 전경 콘텐츠를 강조합니다.

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_brightness=-10&layer=1&src=myRootId/myImageId`
