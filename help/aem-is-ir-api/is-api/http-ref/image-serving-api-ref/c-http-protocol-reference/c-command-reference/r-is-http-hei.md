---
title: hei
description: 보기 높이. 요청에 맞춤 기능이 없을 때 응답 이미지(이미지 보기)의 높이를 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c812c7f0-4ac1-42cb-be47-7baebd8caf60
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 2%

---

# hei{#hei}

보기 높이. 요청에 맞춤 기능이 없을 때 응답 이미지(이미지 보기)의 높이를 지정합니다.

` hei= *`val`*`

<table id="simpletable_1A36827B6E6647888A4E6E868975D716"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var </span> </span> </p> </td> 
  <td class="stentry"> <p>이미지 높이, 픽셀 단위(정수: 0보다 큼). </p> </td> 
 </tr> 
</table>

둘 다인 경우 `wid=` 및 `scl=` 지정된 경우 합성 이미지는 다음 내용에 따라 잘릴 수 있습니다. `align=`특성. 날짜 `fit=` 이(가) 있음, `hei=` 정확한 응답 이미지 높이, 최소 또는 최대 응답 이미지 높이를 지정합니다. 다음에 대한 설명을 참조하십시오. [맞춤=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md) 을 참조하십시오.

If `scl=` 를 지정하지 않으면 합성 이미지가 크기에 맞게 조정됩니다. 둘 다인 경우 `wid=` 및 `hei=` 및 `scl=` 가 지정되지 않은 경우 이미지는 wid/hei 사각형 내에 완전히 맞게 크기가 조정되어 배경 영역이 가능한 한 적게 노출됩니다. 이 경우 이미지는 다음에 따라 보기 사각형 내에 배치됩니다. `align=` 특성. 배경 영역이 다음으로 채워짐 `bgc=`, 또는 로 지정되지 않은 경우 `attribute::BkgColor`.

>[!NOTE]
>
>계산된 응답 이미지 크기가 보다 큰 경우 오류가 반환됩니다 `attribute::MaxPix`.

## 속성 {#section-534923644a1e464496eeba83dedcbd3c}

속성 보기. 현재 레이어 설정에 관계없이 적용됩니다.

## 기본값 {#section-76544d34806d4124a8b173e229cba71f}

둘 다 아닌 경우 `wid=`, `hei=`, 또는 `scl=` 지정된 경우 응답 이미지의 크기가 합성 이미지 또는 `attribute::DefaultPix`, 둘 중 더 작은 것입니다.

## 예제 {#section-eb10df7cd67e4733984810aaffd0b9e2}

이미지를 200x200 사각형에 맞추도록 요청하고, 사각형이 아닌 경우 이미지를 왼쪽 위로 정렬합니다. 모든 배경 영역이 다음으로 채워짐 `attribute::BkgColor`.

`http://server/myRootId/myImageId?wid=200&hei=200&align=-1,-1`

동일한 이미지가 200픽셀의 고정된 높이에서 전달되지만 이미지의 종횡비에 맞게 너비가 달라집니다. 이 경우 반환된 이미지에 배경 채우기 영역이 없습니다. 이 경우 참고 사항 `align=` 전혀 효과가 없을 겁니다.

`http://server/myRootId/myImageId?hei=200`

## 참조 {#section-796e059e42ea4e86ab90ea3d024850ec}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [맞춤=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [정렬=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), [rgn=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f), [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1), [attribute::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
