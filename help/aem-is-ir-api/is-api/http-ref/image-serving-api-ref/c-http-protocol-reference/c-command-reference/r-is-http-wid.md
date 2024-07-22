---
title: wid
description: 보기 너비. fit=이 요청에 없을 때 응답 이미지(이미지 보기)의 너비를 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ba22c79b-da59-4993-aa1c-2c990a0c4be5
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 1%

---

# wid{#wid}

보기 너비. fit=이 요청에 없을 때 응답 이미지(이미지 보기)의 너비를 지정합니다.

`wid= *`val`*`

<table id="simpletable_E217453246F5441C896C1F69EA4D4218"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 값 </span> </p> </td> 
  <td class="stentry"> <p>이미지 너비, 픽셀 단위(int가 0보다 큼). </p> </td> 
 </tr> 
</table>

`hei=`과(와) `scl=`을(를) 모두 지정하면 `align=` 특성에 따라 합성 이미지가 잘릴 수 있습니다. `fit=`이(가) 있는 경우 `wid=`은(는) 정확한 응답, 최소 또는 최대 응답 이미지 폭을 지정합니다. 자세한 내용은 `fit=`의 설명을 참조하십시오.

`scl=`을(를) 지정하지 않으면 합성 이미지가 맞춰집니다. `wid=`과(와) `hei=`을(를) 모두 지정하고 `scl=`을(를) 지정하지 않으면 이미지가 wid/hei 사각형에 완전히 맞게 조정되어 배경 영역이 최대한 적게 노출됩니다. 이 경우 이미지는 `align=` 특성에 따라 보기 사각형 내에 배치됩니다.

>[!NOTE]
>
>계산 또는 기본 응답 이미지 크기가 `attribute::MaxPix`보다 큰 경우 오류가 반환됩니다.

## 기본값 {#section-976d4c8554a34c899f85d172f6ac6f58}

`wid=`, `hei=` 및 `scl=`이(가) 모두 지정되지 않은 경우 응답 이미지의 크기가 합성 이미지 또는 `attribute::DefaultPix` 중 더 작은 것입니다.

## 속성 {#section-c93b7ce1b0d2475f80b06264b45d1285}

속성 보기. 이 설정은 현재 레이어 설정에 관계없이 적용됩니다.

## 예 {#section-82bc98b7c15a451bbe9b915d414c0470}

200x200 사각형에 맞게 이미지를 요청하고 정사각형이 아닌 경우 이미지를 오른쪽 위로 정렬합니다. 모든 배경 영역이 `attribute::BkgColor`(으)로 채워져 있습니다.

` http:// *`서버`*/myRootId/myImageId?wid=200&hei=200&align=1,-1`

동일한 이미지가 200픽셀의 고정된 너비로 전달되지만 이미지의 종횡비를 유지하기 위해 높이가 달라집니다. 이 경우 반환된 이미지에 배경 채우기 영역이 없습니다. 이 경우 `align=`은(는) 전혀 영향을 주지 않습니다.

` http:// *`서버`*/myRootId/myImageId?wid=200`

## 참조 {#section-4e9659238d6545498378ca8b1f3ec4ae}

[hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96) , [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7), [특성::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1), [특성::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
