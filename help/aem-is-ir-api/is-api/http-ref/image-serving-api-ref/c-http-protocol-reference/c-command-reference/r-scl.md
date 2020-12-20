---
description: 비율 보기. 복합 이미지를 invFactor의 역값으로 비율을 조정합니다.
seo-description: 비율 보기. 복합 이미지를 invFactor의 역값으로 비율을 조정합니다.
seo-title: scl
solution: Experience Manager
title: scl
topic: Scene7 Image Serving - Image Rendering API
uuid: 10a365dc-9fc1-4236-9528-4aca04a4ca19
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 5%

---


# scl{#scl}

비율 보기. 복합 이미지를 invFactor의 역값으로 비율을 조정합니다.

`scl= *`invFactor`*`

<table id="simpletable_A09F5EECAC2B4E0F8633D71C6AD36D8D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> invFactor</span> </p> </td> 
  <td class="stentry"> <p>역배율 계수(0.0보다 큼). </p></td> 
 </tr> 
</table>

`scl=1` 시에는 크기 조절이 적용되지 않습니다. *`invFactor`* 1.0보다 크고 1.0보다 작으면 합성 이미지가 확대됩니다.

`scl=`이 지정되어 있고 `wid=` 및/또는 `hei=`도 함께 있는 경우 이미지가 비율 조정 후 `wid=` 및/또는 `hei=`로 잘립니다.

>[!NOTE]
>
>계산된 이미지 또는 기본 답글 이미지 크기가 `attribute::MaxPix`보다 크면 오류가 반환됩니다.

## 속성 {#section-60af012719db477db4a4703e9a6da5f5}

속성 보기를 참조하십시오. 현재 레이어 설정에 관계없이 적용됩니다.

## 기본값 {#section-32502fa218a24e1f9c65f41c0260b56a}

`wid=`, `hei=` 또는 `scl=`가 지정되지 않은 경우 응답 이미지의 크기가 합성 이미지의 크기나 `attribute::DefaultPix` 중 더 작은 이미지를 가지게 됩니다.

## 예 {#section-a33f6239476a4b438d939656ad99aa76}

`scl=`의 일반적인 응용 프로그램에 대해서는 [rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096)의 예제를 참조하십시오.

## 참조 {#section-ccefd5de59924059903d66d4974ce317}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [속성::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)
