---
description: 텍스처를 선명하게 합니다. 이 자료를 렌더링할 때 적용할 선명하게 하기를 지정합니다.
solution: Experience Manager
title: 날카로운
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 7921ceba-e249-4aab-823e-c54705c4a7c3
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 6%

---

# 날카로운{#sharp}

텍스처를 선명하게 합니다. 이 자료를 렌더링할 때 적용할 선명하게 하기를 지정합니다.

`sharp=0|1|2|3`

<table id="simpletable_04B4EAA7CE7D4ED48A61A50CD001388F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>선명하게 하지 않습니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>일반 선명하게 하기(늦게). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>0개의 대체 선명하게 하기(조기) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>더 선명하게 하기(일찍 및 늦게). </p> </td> 
 </tr> 
</table>

`sharp=1` 소재가 렌더링된 후 선명하게 적용 `sharp=2` 텍스처의 초기 비율 조정 후 선명도 적용하지만 장면으로 변환하기 전에 선명도 적용 `sharp=3` 변환 전 및 후에 선명도 적용

선명하게 하기 알고리즘 및 선명하게 하기 및 기타 USM(언샵 마스킹) 매개 변수는 비네팅 또는 `rs=`으로 제공된 기본 재료 템플릿에 의해 제어됩니다.

## 속성 {#section-498ec9fcb8eb415fb99532d36c11d4c7}

재료 속성입니다. 단색 재료에서 무시됨.

## 기본값 {#section-febfa16e65864987b4d328e2ff1df64d}

`catalog::Sharp`로 지정하는 경우, 해당 자료가 카탈로그 항목을 기반으로 하는 경우 그렇지 않은 경우  `attribute::Sharp`.

## 참조 {#section-0d5e2c94342c4ee586374ad9c917eeb9}

[catalog::Sharp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-sharp-dataref.md#reference-f79a14bd52474dfd8495115d398a30d0) ,  [선명하게=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharpen.md#reference-13034d22d176483cb99ccafc2a4f6a6e),  [rs=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rs.md#reference-d20cefaaa6cd4f449d1591c87959b4cf)
