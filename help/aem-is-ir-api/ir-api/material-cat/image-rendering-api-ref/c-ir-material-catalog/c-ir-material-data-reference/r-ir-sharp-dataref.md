---
description: 선명하게 하기. Sharpening 속성을 사용하여 렌더링하는 동안 질감이 선명하게 되는 시기를 결정합니다.
seo-description: 선명하게 하기. Sharpening 속성을 사용하여 렌더링하는 동안 질감이 선명하게 되는 시기를 결정합니다.
seo-title: 샤프
solution: Experience Manager
title: 샤프
topic: Scene7 Image Serving - Image Rendering API
uuid: f153f496-f2c5-43d0-a7f0-00045fd96af8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 선명하게 {#sharp}

선명하게 하기. Sharpening 속성을 사용하여 렌더링하는 동안 질감이 선명하게 되는 시기를 결정합니다.

선명하게 하기 유형 및 양은 기본 재료 템플릿 또는 를 통해 비네팅을 통해 제어됩니다 `catalog::RenderSettings`.

## 속성 {#section-aac81b1a611b4bca90b8544eae7896df}

열거형.

<table id="simpletable_D52B41A39E4E4E54A06821B9D689DB30"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>선명하게 하기 없음 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>일반적인 선명하게 하기(변환 후). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>대체 선명하게 하기(변환 전). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>더 선명하게 하기(변형 전과 후 모두). </p></td> 
 </tr> 
</table>

단색 재질로 무시되며 다른 모든 재질에는 선택 사항입니다.

## 기본값 {#section-a6bc204d552b4cc3ae6a77ec232c26ff}

`attribute::Sharpening` 값이 없거나, 필드가 비어 있거나, 값이 지원되는 선택 항목 중 하나가 아닌 경우 사용됩니다.

## 참조 {#section-b462f9ad9ae347e1a1993abf2f2daa8e}

[attribute::Sharpening](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-sharp.md#reference-c706450cf95347f98f86c696f9167297) , [catalog::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rendersettings.md#reference-f3ae5e18095d40b2a8edef957dd82fbd), [sharp=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a)
