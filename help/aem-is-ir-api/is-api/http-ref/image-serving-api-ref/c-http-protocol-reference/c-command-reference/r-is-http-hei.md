---
description: 보기 높이. 요청에 fit가 없을 때 응답 이미지(이미지 보기)의 높이를 지정합니다.
seo-description: 보기 높이. 요청에 fit가 없을 때 응답 이미지(이미지 보기)의 높이를 지정합니다.
seo-title: hei
solution: Experience Manager
title: hei
topic: Scene7 Image Serving - Image Rendering API
uuid: 307952bb-604f-49b4-bce3-b7a7fc7ec63b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# hei{#hei}

보기 높이. 요청에 fit가 없을 때 응답 이미지(이미지 보기)의 높이를 지정합니다.

` hei= *`val`*`

<table id="simpletable_1A36827B6E6647888A4E6E868975D716"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var </span></span> </p> </td> 
  <td class="stentry"> <p>이미지 높이(픽셀 단위: 0보다 큼). </p> </td> 
 </tr> 
</table>

과 `wid=` 를 모두 `scl=` 지정하면 합성 이미지가 `align=`속성에 따라 잘릴 수 있습니다. 가 `fit=` 있을 때 `hei=` 정확한, 최소 또는 최대 응답 이미지 높이를 지정합니다.자세한 내용은 의 설명을 ` [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)` 참조하십시오.

이 `scl=` 값을 지정하지 않으면 합성 이미지가 크기에 맞게 조정됩니다. 둘 다 `wid=` 및 `hei=` 를 모두 지정하고 지정하지 `scl=` 않으면 이미지 크기가 wid/hei 사각형 내에 완전히 맞게 조절되므로 가능한 한 작은 배경 영역이 노출됩니다.이 경우 이미지는 속성에 따라 보기 사각형 내에 배치됩니다 `align=` . 배경 영역은 `bgc=`또는 으로 지정하지 않은 경우 으로 채워집니다 `attribute::BkgColor`.

>[!NOTE]
>
>계산된 응답 이미지 크기가 다음보다 큰 경우 오류가 반환됩니다 `attribute::MaxPix`.

## 속성 {#section-534923644a1e464496eeba83dedcbd3c}

속성을 봅니다. 현재 레이어 설정에 관계없이 적용됩니다.

## 기본값 {#section-76544d34806d4124a8b173e229cba71f}

둘 다 `wid=`지정하지 `hei=`않거나 `scl=` 지정하지 않으면 응답 이미지의 크기가 합성 이미지 또는 `attribute::DefaultPix`둘 중 더 작습니다.

## 예제 {#section-eb10df7cd67e4733984810aaffd0b9e2}

200x200 사각형에 맞게 이미지를 요청합니다.정사각형이 아닌 경우 이미지를 왼쪽 위로 정렬합니다. 모든 배경 영역이 `attribute::BkgColor`채워집니다.

`http://server/myRootId/myImageId?wid=200&hei=200&align=-1,-1`

200픽셀의 고정된 높이로 전달되는 동일한 이미지만, 이미지의 종횡비와 일치하는 가변 폭을 사용합니다. 이 경우 반환된 이미지에는 배경 채우기 영역이 없습니다. 이 경우에는 아무런 `align=` 효과가 없습니다.

`http://server/myRootId/myImageId?hei=200`

## 참조 {#section-796e059e42ea4e86ab90ea3d024850ec}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) fit= [,](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)scl= [,](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)align= [,](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88)[align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f)[](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)[, bgc, rgn=0, lynx, Attribute::defaultPixDefault Pix, MaxPipix 속성:](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
