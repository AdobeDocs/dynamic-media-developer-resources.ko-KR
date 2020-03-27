---
description: 확대 보기. invFactor의 역함수를 기준으로 합성 이미지의 크기를 조정합니다.
seo-description: 확대 보기. invFactor의 역함수를 기준으로 합성 이미지의 크기를 조정합니다.
seo-title: scl
solution: Experience Manager
title: scl
topic: Scene7 Image Serving - Image Rendering API
uuid: 10a365dc-9fc1-4236-9528-4aca04a4ca19
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# scl{#scl}

확대 보기. invFactor의 역함수를 기준으로 합성 이미지의 크기를 조정합니다.

`scl= *`invFactor`*`

<table id="simpletable_A09F5EECAC2B4E0F8633D71C6AD36D8D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> invFactor</span> </p> </td> 
  <td class="stentry"> <p>역배율 인수(0.0보다 실제). </p></td> 
 </tr> 
</table>

No scaling is applied when `scl=1`. *`invFactor`* 1.0보다 크고 1.0보다 작으면 합성 이미지가 확대됩니다.

이 `scl=` 지정되고 `wid=` 및/또는 `hei=` 이 함께 있는 경우 이미지가 크기 조절 후 `wid=` 및/또는 `hei=` 로 잘립니다.

>[!NOTE]
>
>계산된 이미지 또는 기본 회신 이미지 크기가 `attribute::MaxPix`다음보다 큰 경우 오류가 반환됩니다.

## 속성 {#section-60af012719db477db4a4703e9a6da5f5}

속성 보기를 참조하십시오. 현재 레이어 설정에 관계없이 적용됩니다.

## 기본값 {#section-32502fa218a24e1f9c65f41c0260b56a}

둘 다 `wid=`지정하지 `hei=`않거나 `scl=` 지정하지 않으면 응답 이미지의 크기가 합성 이미지 또는 `attribute::DefaultPix`둘 중 더 작은 이미지 중 하나를 갖습니다.

## 예 {#section-a33f6239476a4b438d939656ad99aa76}

의 일반적인 응용 프로그램에 대해서는 [rotate=의](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) 예를 `scl=`참조하십시오.

## 참조 {#section-ccefd5de59924059903d66d4974ce317}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [속성::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)
