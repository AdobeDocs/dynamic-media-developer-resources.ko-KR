---
description: 보기 높이. 요청에 fit가 없을 때 응답 이미지(보기 이미지)의 높이를 지정합니다.
solution: Experience Manager
title: hei
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c812c7f0-4ac1-42cb-be47-7baebd8caf60
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 3%

---

# 헤이{#hei}

보기 높이. 요청에 fit가 없을 때 응답 이미지(보기 이미지)의 높이를 지정합니다.

` hei= *`val`*`

<table id="simpletable_1A36827B6E6647888A4E6E868975D716"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var  </span> </span> </p> </td> 
  <td class="stentry"> <p>이미지 높이(픽셀 단위)가 0보다 큼. </p> </td> 
 </tr> 
</table>

`wid=` 및 `scl=`이 모두 지정된 경우 합성 이미지가 `align=`특성에 따라 잘릴 수 있습니다. `fit=`이 있으면 `hei=`에서 정확한 응답 이미지, 최소 또는 최대 응답 이미지 높이를 지정합니다. 자세한 내용은 ` [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)`의 설명을 참조하십시오.

`scl=` 을 지정하지 않으면 합성 이미지의 크기가 적절히 조절됩니다. `wid=` 및 `hei=`이 모두 지정되어 있고 `scl=`가 지정되지 않은 경우 이미지 크기가 wid/hei 사각형 내에 완전히 맞게 조정되며 가능한 한 적은 배경 영역이 노출됩니다. 이 경우 이미지는 `align=` 속성에 따라 보기 사각형 내에 배치됩니다. 배경 영역은 `bgc=` 또는 `attribute::BkgColor` 로 지정되지 않은 경우 로 채워집니다.

>[!NOTE]
>
>계산된 회신 이미지 크기가 `attribute::MaxPix`보다 큰 경우 오류가 반환됩니다.

## 속성 {#section-534923644a1e464496eeba83dedcbd3c}

속성 보기. 현재 레이어 설정에 관계없이 적용됩니다.

## 기본값 {#section-76544d34806d4124a8b173e229cba71f}

`wid=`, `hei=` 및 `scl=`를 지정하지 않은 경우, 회신 이미지의 크기는 합성 이미지의 크기나 `attribute::DefaultPix` 중 작은 이미지 중 하나를 갖습니다.

## 예제 {#section-eb10df7cd67e4733984810aaffd0b9e2}

200x200 사각형에 맞게 이미지를 요청합니다. 이미지가 사각형이 아닌 경우 왼쪽 위에서 이미지를 정렬합니다. 모든 배경 영역은 `attribute::BkgColor` 로 채워집니다.

`http://server/myRootId/myImageId?wid=200&hei=200&align=-1,-1`

고정된 높이 200픽셀로 전달되지만 이미지의 종횡비에 맞게 가변 너비가 제공되는 동일한 이미지입니다. 이 경우 반환된 이미지에는 배경 채우기 영역이 없습니다. 이 경우 `align=`은 전혀 영향을 주지 않습니다.

`http://server/myRootId/myImageId?hei=200`

## 참조 {#section-796e059e42ea4e86ab90ea3d024850ec}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7),  [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88),  [rgn=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f),  [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1),  [attribute::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
