---
title: scl
description: 크기 조절 보기. invFactor의 역순으로 합성 이미지의 배율을 조정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 297d187c-3a52-45ff-b73d-0b0e4b956080
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 2%

---

# scl{#scl}

크기 조절 보기. invFactor의 역순으로 합성 이미지의 배율을 조정합니다.

`scl= *`invFactor`*`

<table id="simpletable_A09F5EECAC2B4E0F8633D71C6AD36D8D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> invFactor</span> </p> </td> 
  <td class="stentry"> <p>역배율 계수(0.0보다 큰 실수). </p></td> 
 </tr> 
</table>

`scl=1`일 때는 크기 조정이 적용되지 않습니다. 1.0보다 크고 1.0보다 작은 *`invFactor`* 값은 합성 이미지를 확대합니다.

`scl=`이(가) 지정되어 있고 `wid=` 및/또는 `hei=`도 있는 경우 크기 조정 후 이미지가 `wid=` 및/또는 `hei=`(으)로 잘립니다.

>[!NOTE]
>
>계산 또는 기본 응답 이미지 크기가 `attribute::MaxPix`보다 큰 경우 오류가 반환됩니다.

## 속성 {#section-60af012719db477db4a4703e9a6da5f5}

속성 보기. 이 설정은 현재 레이어 설정에 관계없이 적용됩니다.

## 기본값 {#section-32502fa218a24e1f9c65f41c0260b56a}

`wid=`, `hei=` 및 `scl=`이(가) 모두 지정되지 않은 경우 응답 이미지의 크기가 합성 이미지 또는 `attribute::DefaultPix` 중 더 작은 것입니다.

## 예 {#section-a33f6239476a4b438d939656ad99aa76}

[의 일반 응용 프로그램에 대해서는 ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096)rotate=`scl=`의 예제를 참조하십시오.

## 참조 {#section-ccefd5de59924059903d66d4974ce317}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [특성::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)
