---
title: op_blur
description: 흐림 효과 이미지입니다. 이미지 데이터에 흐림 효과 필터를 적용합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: cd68c109-ee99-4ef7-aac0-7d2e6d408cc0
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 2%

---

# op_blur{#op-blur}

흐림 효과 이미지입니다. 이미지 데이터에 흐림 효과 필터를 적용합니다.

`op_blur= *`반경`*`

<table id="simpletable_1DD41D819BE74130A77ECFC28486F70A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 반경</span> </p> </td> 
  <td class="stentry"> <p>픽셀 단위 흐림 필터 반경(실수 0..100). </p></td> 
 </tr> 
</table>

*`radius`*&#x200B;은(는) 합성 이미지를 기준으로 픽셀 단위입니다. 레이어 효과를 페더링하는 데에도 사용됩니다.

## 속성 {#section-92573fe2c07746a7bab93a81fc3d208d}

레이어 명령. `layer=comp`인 경우 현재 레이어 또는 합성 이미지에 적용됩니다.

## 기본값 {#section-a976cb86620d489085a8fc9bae2626c0}

흐림 효과 없이 `op_blur=0`.

## 예 {#section-1ebacde68388492eb108ae0fcd7424db}

이미지의 배경을 흐리게 합니다. `catalog::MaskPath`에서 별도의 마스크 이미지를 참조합니다. `layer=0`을(를) 명시적으로 지정해야 합니다. 그렇지 않으면 `op_blur`이(가) 전체 합성 이미지에 적용됩니다.

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_blur=20&layer=1&src=myRootId/myImageId`
