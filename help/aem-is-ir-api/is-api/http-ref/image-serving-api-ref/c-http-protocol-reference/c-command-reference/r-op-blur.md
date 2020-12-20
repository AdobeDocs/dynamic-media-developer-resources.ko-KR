---
description: 흐림 이미지. 이미지 데이터에 흐림 필터를 적용합니다.
seo-description: 흐림 이미지. 이미지 데이터에 흐림 필터를 적용합니다.
seo-title: op_blur
solution: Experience Manager
title: op_blur
topic: Scene7 Image Serving - Image Rendering API
uuid: 8405bbb5-fe09-412e-9b52-0af2c01f48b9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 2%

---


# op_blur{#op-blur}

흐림 이미지. 이미지 데이터에 흐림 필터를 적용합니다.

`op_blur= *`반경`*`

<table id="simpletable_1DD41D819BE74130A77ECFC28486F70A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 반경</span> </p> </td> 
  <td class="stentry"> <p>흐림 필터 반경(픽셀 단위)(실제 0.100). </p></td> 
 </tr> 
</table>

*`radius`* 합성 이미지를 기준으로 픽셀 단위로 표시합니다. 레이어 효과를 페더링하는 데에도 사용됩니다.

## 속성 {#section-92573fe2c07746a7bab93a81fc3d208d}

레이어 명령. `layer=comp`인 경우 현재 레이어나 합성 이미지에 적용됩니다.

## 기본값 {#section-a976cb86620d489085a8fc9bae2626c0}

`op_blur=0`를 선택합니다.

## 예 {#section-1ebacde68388492eb108ae0fcd7424db}

이미지의 배경을 흐리게 합니다. 별도의 마스크 이미지가 `catalog::MaskPath`에서 참조됩니다. `layer=0`은 명시적으로 지정해야 하며, 그렇지 않으면 `op_blur`은 전체 합성 이미지에 적용됩니다.

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_blur=20&layer=1&src=myRootId/myImageId`
