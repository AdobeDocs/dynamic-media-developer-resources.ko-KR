---
title: 예리하
description: 텍스처를 선명하게 합니다. 이 재료를 렌더링할 때 적용할 선명하게 하기를 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7921ceba-e249-4aab-823e-c54705c4a7c3
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 5%

---

# 예리하{#sharp}

텍스처를 선명하게 합니다. 이 재료를 렌더링할 때 적용할 선명하게 하기를 지정합니다.

`sharp=0|1|2|3`

<table id="simpletable_04B4EAA7CE7D4ED48A61A50CD001388F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>선명하게 하지 않습니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>일반 선명하게 하기(지연). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>0 대체 선명하게 하기(조기). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>더 선명하게 하기(이른 및 늦은). </p> </td> 
 </tr> 
</table>

`sharp=1` 재료가 렌더링된 후에 선명하게 하기를 적용하고, `sharp=2`이(가) 텍스처의 초기 크기 조절 후에 선명하게 하기를 적용하고, 장면으로 변형되기 전에 선명하게 하기를 적용하고, `sharp=3`은(는) 변형 전후에 선명하게 하기를 적용합니다.

선명하게 하기 알고리즘 및 선명하게 하기 및 기타 USM(언샵 마스킹) 매개 변수의 양은 비네팅 또는 `rs=`에서 제공하는 기본 재질 템플릿에 의해 제어됩니다.

## 속성 {#section-498ec9fcb8eb415fb99532d36c11d4c7}

재질 속성입니다. 단색 소재에서 무시됨.

## 기본값 {#section-febfa16e65864987b4d328e2ff1df64d}

`catalog::Sharp`(자료가 카탈로그 항목을 기반으로 하는 경우), 그렇지 않으면 `attribute::Sharp`.

## 참조 {#section-0d5e2c94342c4ee586374ad9c917eeb9}

[카탈로그::Sharp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-sharp-dataref.md#reference-f79a14bd52474dfd8495115d398a30d0) , [sharpen=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharpen.md#reference-13034d22d176483cb99ccafc2a4f6a6e), [rs=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rs.md#reference-d20cefaaa6cd4f449d1591c87959b4cf)
