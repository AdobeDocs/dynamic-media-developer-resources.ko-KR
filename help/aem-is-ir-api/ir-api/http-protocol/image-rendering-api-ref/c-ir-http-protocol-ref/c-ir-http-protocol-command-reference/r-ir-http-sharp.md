---
description: 텍스처를 선명하게 합니다. 이 자료를 렌더링할 때 적용할 선명 효과를 지정합니다.
seo-description: 텍스처를 선명하게 합니다. 이 자료를 렌더링할 때 적용할 선명 효과를 지정합니다.
seo-title: sharp
solution: Experience Manager
title: sharp
topic: Scene7 Image Serving - Image Rendering API
uuid: 8265eebf-9cec-4ad3-8b22-0f46f33a89f1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# sharp{#sharp}

텍스처를 선명하게 합니다. 이 자료를 렌더링할 때 적용할 선명 효과를 지정합니다.

`sharp=0|1|2|3`

<table id="simpletable_04B4EAA7CE7D4ED48A61A50CD001388F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>선명하게 하기 없음 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>일반 선명하게 하기(지연). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>0개의 대체 선명하게 하기(조기). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>선명하게 하기(조기 및 지연). </p> </td> 
 </tr> 
</table>

`sharp=1` 재질이 렌더링된 후 선명하게 하기텍스처의 초기 크기 조절 후 선명 효과를 `sharp=2` 적용하지만 장면으로 변환되기 전에 선명하게 합니다.변환 전과 후에 선명하게 `sharp=3` 하기를 적용합니다.

선명하게 하기 알고리즘, 선명하게 하기 및 기타 USM(언샵 마스킹) 매개 변수는 비네팅 또는 에서 제공하는 기본 재료 템플릿에 의해 제어됩니다 `rs=`.

## 속성 {#section-498ec9fcb8eb415fb99532d36c11d4c7}

재료 속성. 단색 재질로 무시됩니다.

## 기본값 {#section-febfa16e65864987b4d328e2ff1df64d}

`catalog::Sharp`, if the material is based on a catalog entry, or otherwise `attribute::Sharp`.

## 참조 {#section-0d5e2c94342c4ee586374ad9c917eeb9}

[catalog::Sharp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-sharp-dataref.md#reference-f79a14bd52474dfd8495115d398a30d0) , [sharpen=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharpen.md#reference-13034d22d176483cb99ccafc2a4f6a6e), [rs=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rs.md#reference-d20cefaaa6cd4f449d1591c87959b4cf)
