---
description: 흐림 효과 이미지. 이미지 데이터에 흐림 효과 필터를 적용합니다.
solution: Experience Manager
title: op_blur
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: cd68c109-ee99-4ef7-aac0-7d2e6d408cc0
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 3%

---

# op_blur{#op-blur}

흐림 효과 이미지. 이미지 데이터에 흐림 효과 필터를 적용합니다.

`op_blur= *`반경`*`

<table id="simpletable_1DD41D819BE74130A77ECFC28486F70A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 반경</span> </p> </td> 
  <td class="stentry"> <p>필터 반경(픽셀 단위)은 흐림(실수 0.100)입니다. </p></td> 
 </tr> 
</table>

*`radius`* 합성 이미지에 대해 픽셀 단위 입니다. 레이어 효과를 페더링하는 데에도 사용됩니다.

## 속성 {#section-92573fe2c07746a7bab93a81fc3d208d}

레이어 명령. `layer=comp` 인 경우 현재 레이어 또는 복합 이미지에 적용됩니다.

## 기본값 {#section-a976cb86620d489085a8fc9bae2626c0}

`op_blur=0`: 흐림 효과 없음

## 예 {#section-1ebacde68388492eb108ae0fcd7424db}

이미지의 배경을 흐리게 합니다. 별도의 마스크 이미지를 `catalog::MaskPath`에서 참조합니다. `layer=0`을 명시적으로 지정해야 하며, 그렇지 않으면 `op_blur`이 전체 합성 이미지에 적용됩니다.

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_blur=20&layer=1&src=myRootId/myImageId`
