---
title: scl
description: 크기 조절 보기. invFactor의 역순으로 합성 이미지의 배율을 조정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 297d187c-3a52-45ff-b73d-0b0e4b956080
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 4%

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

다음과 같은 경우에는 배율이 적용되지 않습니다. `scl=1`. *`invFactor`* 축소율이 1.0보다 크고 축소율이 1.0보다 작으면 합성 이미지가 확대됩니다.

If `scl=` 이(가) 지정되고, `wid=` 및/또는 `hei=` 이(가) 있으면 이미지가 잘립니다. `wid=` 및/또는 `hei=` 배율 조정 후.

>[!NOTE]
>
>계산 또는 기본 응답 이미지 크기가 보다 큰 경우 오류가 반환됩니다 `attribute::MaxPix`.

## 속성 {#section-60af012719db477db4a4703e9a6da5f5}

속성 보기. 현재 레이어 설정에 관계없이 적용됩니다.

## 기본값 {#section-32502fa218a24e1f9c65f41c0260b56a}

둘 다 아닌 경우 `wid=`, `hei=`, 또는 `scl=` 이(가) 지정되면 응답 이미지의 크기가 합성 이미지 또는 `attribute::DefaultPix`, 둘 중 더 작은 것입니다.

## 예 {#section-a33f6239476a4b438d939656ad99aa76}

의 예제를 참조하십시오. [회전=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) 의 공통 적용을 위해 `scl=`.

## 참조 {#section-ccefd5de59924059903d66d4974ce317}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)
