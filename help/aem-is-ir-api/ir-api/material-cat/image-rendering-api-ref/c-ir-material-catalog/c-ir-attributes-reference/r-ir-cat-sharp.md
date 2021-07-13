---
description: 기본 재료 선명하게 하기. 특정 카탈로그 레코드에 유효한 카탈로그 Sharp 값이 포함되지 않은 경우 기본 자재 선명하게 하기 모드를 설정합니다.
solution: Experience Manager
title: 샤프
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fe8f7662-bfa1-43bf-ab66-5de5598edcd4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 10%

---

# 샤프{#sharp}

기본 재료 선명하게 하기. 특정 카탈로그 레코드에 올바른 카탈로그::Sharp 값이 포함되지 않은 경우 기본 재료 선명하게 하기 모드를 설정합니다.

## 속성 {#section-dcb810d01b8a40eb991d555a3cbe48b9}

열거형.

<table id="simpletable_2D94A380BC2D4FD1A7EDD45E6EAFD1FB"> 
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
  <td class="stentry"> <p>더 선명하게 하기(변형 전후에 모두). </p> </td> 
 </tr> 
</table>

## 기본값 {#section-613130fca7c04ce7a7734265f27aa1ea}

정의되지 않았거나 비어 있는 경우 `default::Sharp`에서 상속됩니다.

## 참조 {#section-7771824f2822443ab0297e8793bb48ae}

[catalog::Sharp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-sharp-dataref.md#reference-f79a14bd52474dfd8495115d398a30d0) ,  [sharp=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a),  [catalog::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-rendersettings-dataref.md#reference-9ce753ae4096455eadcc12ac064de711)
