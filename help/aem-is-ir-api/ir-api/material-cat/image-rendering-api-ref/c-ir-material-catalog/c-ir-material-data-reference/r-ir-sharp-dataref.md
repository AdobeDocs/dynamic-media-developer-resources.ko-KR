---
description: 선명하게 하기. 선명하게 하기 속성은 렌더링 중에 재료가 선명하게 되는 시기를 결정합니다.
solution: Experience Manager
title: 샤프
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ce08ed97-33b7-4d28-8f7f-3f3ef8598ad6
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 8%

---

# 샤프{#sharp}

선명하게 하기. 선명하게 하기 속성은 렌더링 중에 재료가 선명하게 되는 시기를 결정합니다.

선명하게 하기 유형 및 양은 기본 재질 템플릿 또는 `catalog::RenderSettings`을(를) 사용하여 비네팅으로 제어됩니다.

## 속성 {#section-aac81b1a611b4bca90b8544eae7896df}

열거형.

<table id="simpletable_D52B41A39E4E4E54A06821B9D689DB30"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>선명하게 하지 않습니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>보통 선명하게 하기(변환 후). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>대체 선명하게 하기(변환 전). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>더 선명하게 하기(변형 전후의 두 가지 모두). </p></td> 
 </tr> 
</table>

단색 소재에서는 무시되며 다른 모든 소재에는 선택 사항입니다.

## 기본값 {#section-a6bc204d552b4cc3ae6a77ec232c26ff}

필드가 없거나 비어 있거나 값이 지원되는 선택 항목 중 하나가 아닌 경우 `attribute::Sharpening`이(가) 사용됩니다.

## 참조 {#section-b462f9ad9ae347e1a1993abf2f2daa8e}

[특성::Sharpening](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-sharp.md#reference-c706450cf95347f98f86c696f9167297) , [카탈로그::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rendersettings.md#reference-f3ae5e18095d40b2a8edef957dd82fbd), [sharp=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a)
