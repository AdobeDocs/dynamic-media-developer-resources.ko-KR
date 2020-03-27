---
description: 보기 너비. fit=가 요청에 없을 때 응답 이미지(이미지 보기)의 너비를 지정합니다.
seo-description: 보기 너비. fit=가 요청에 없을 때 응답 이미지(이미지 보기)의 너비를 지정합니다.
seo-title: wid
solution: Experience Manager
title: wid
topic: Scene7 Image Serving - Image Rendering API
uuid: 30aeeea0-c8c9-40b9-a244-2802a7102dd6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# wid{#wid}

보기 너비. fit=가 요청에 없을 때 응답 이미지(이미지 보기)의 너비를 지정합니다.

` wid= *`val`*`

<table id="simpletable_E217453246F5441C896C1F69EA4D4218"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>이미지 너비(픽셀 단위: 0보다 큼) </p> </td> 
 </tr> 
</table>

과 `hei=` 를 모두 `scl=` 지정하면 합성 이미지가 `align=` 속성에 따라 잘릴 수 있습니다. 가 `fit=` 있을 때 `wid=` 정확한, 최소 또는 최대 응답 이미지 너비를 지정합니다.자세한 내용은 의 설명을 `fit=` 참조하십시오.

이 `scl=` 값을 지정하지 않으면 합성 이미지가 크기에 맞게 조정됩니다. 둘 다 `wid=` 및 `hei=` 를 모두 지정하고 지정하지 `scl=` 않으면 배경 영역이 가능한 한 노출되지 않고 전체 너비/헤이 사각형 내에 맞게 이미지가 조정됩니다. 이 경우 이미지는 `align=` 속성에 따라 보기 사각형 내에 배치됩니다.

>[!NOTE]
>
>계산된 이미지 또는 기본 회신 이미지 크기가 `attribute::MaxPix`다음보다 큰 경우 오류가 반환됩니다.

## 기본값 {#section-976d4c8554a34c899f85d172f6ac6f58}

둘 다 `wid=`지정하지 `hei=`않거나 `scl=` 지정하지 않으면 응답 이미지의 크기가 합성 이미지 또는 `attribute::DefaultPix`둘 중 더 작은 이미지 중 하나를 갖습니다.

## 속성 {#section-c93b7ce1b0d2475f80b06264b45d1285}

속성을 봅니다. 현재 레이어 설정에 관계없이 적용됩니다.

## 예 {#section-82bc98b7c15a451bbe9b915d414c0470}

200x200 사각형에 맞게 이미지를 요청합니다.정사각형이 아닌 경우 이미지를 오른쪽 위로 정렬합니다. 모든 배경 영역이 `attribute::BkgColor`채워집니다.

` http:// *`서버`*/myRootId/myImageId?wid=200&hei=200&align=1,-1`

200픽셀의 고정 너비로 전달되는 동일한 이미지만, 이미지의 종횡비를 유지하기 위해 가변 높이를 사용합니다. 이 경우 반환된 이미지에는 배경 채우기 영역이 없습니다. 이 경우 align=은 전혀 영향을 주지 않습니다.

` http:// *`서버`*/myRootId/myImageId?wid=200`

## 참조 {#section-4e9659238d6545498378ca8b1f3ec4ae}

[hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96) fit= [,](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)align= [,](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)align= [,](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)[](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)[attribute::DefaultPixDefaultAttribute::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
