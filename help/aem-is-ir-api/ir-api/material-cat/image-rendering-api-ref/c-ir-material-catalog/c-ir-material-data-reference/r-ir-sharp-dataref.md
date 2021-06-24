---
description: 선명하게 하기. 선명하게 하기 속성을 사용하여 렌더링 중에 재료를 선명하게 하는 시기를 결정합니다.
solution: Experience Manager
title: 샤프
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: ce08ed97-33b7-4d28-8f7f-3f3ef8598ad6
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 10%

---

# 샤프{#sharp}

선명하게 하기. 선명하게 하기 속성을 사용하여 렌더링 중에 재료를 선명하게 하는 시기를 결정합니다.

선명하게 하기 유형 및 양은 기본 재료 템플릿을 통해 또는 `catalog::RenderSettings` 을 사용하여 비네트에 의해 제어됩니다.

## 속성 {#section-aac81b1a611b4bca90b8544eae7896df}

열거형.

<table id="simpletable_D52B41A39E4E4E54A06821B9D689DB30"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>선명하게 하지 않습니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>일반 선명하게 하기(변환 후). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>대체 선명하게 하기(변환 전). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>더 선명하게 하기(변형 전후에 모두). </p></td> 
 </tr> 
</table>

고색 재료에서 무시되고 다른 모든 재료에서 선택 사항입니다.

## 기본값 {#section-a6bc204d552b4cc3ae6a77ec232c26ff}

`attribute::Sharpening` 필드가 없거나 비어 있거나 값이 지원되는 선택 사항 중 하나가 아닌 경우 이 사용됩니다.

## 참조 {#section-b462f9ad9ae347e1a1993abf2f2daa8e}

[attribute::Sharpening](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-sharp.md#reference-c706450cf95347f98f86c696f9167297) ,  [catalog::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rendersettings.md#reference-f3ae5e18095d40b2a8edef957dd82fbd),  [sharp=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a)
