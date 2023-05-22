---
title: 샤프
description: 기본 재질 선명하게 하기. 특정 카탈로그 레코드에 유효한 카탈로그 선명하게 값이 없는 경우 기본 재질 선명하게 하기 모드를 설정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fe8f7662-bfa1-43bf-ab66-5de5598edcd4
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 10%

---

# 샤프{#sharp}

기본 재질 선명하게 하기. 특정 카탈로그 레코드에 유효한 값이 없는 경우 기본 재질 선명하게 하기 모드를 설정합니다. `catalog::Sharp` 값.

## 속성 {#section-dcb810d01b8a40eb991d555a3cbe48b9}

열거형.

<table id="simpletable_2D94A380BC2D4FD1A7EDD45E6EAFD1FB"> 
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
  <td class="stentry"> <p>더 선명하게 하기(변형 전후의 두 가지 모두). </p> </td> 
 </tr> 
</table>

## 기본값 {#section-613130fca7c04ce7a7734265f27aa1ea}

상속 위치 `default::Sharp` 정의되지 않은 경우 또는 비어 있는 경우.

## 참조 {#section-7771824f2822443ab0297e8793bb48ae}

[catalog::Sharp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-sharp-dataref.md#reference-f79a14bd52474dfd8495115d398a30d0) , [sharp=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a), [catalog::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-rendersettings-dataref.md#reference-9ce753ae4096455eadcc12ac064de711)
