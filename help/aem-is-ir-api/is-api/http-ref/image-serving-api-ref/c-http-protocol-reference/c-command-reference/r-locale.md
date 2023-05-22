---
description: 번역 로케일 Id. 요청의 로케일 ID를 지정합니다.
solution: Experience Manager
title: 로케일
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d937dfa5-95dd-49fd-ac23-e77e07b0642c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 4%

---

# 로케일{#locale}

번역 로케일 Id. 요청의 로케일 ID를 지정합니다.

`locale=[ *`locId`*]`

<table id="simpletable_C1899AD02C984ED3896B7620916637E7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> locId</span></span> </p> </td> 
  <td class="stentry"> <p>로케일 ID(문자열). </p></td> 
 </tr> 
</table>

이 ID와 (으)로 지정된 규칙 사용 `attribute::LocaleMap` 및 `attribute::LocaleStrMap`, 이미지 제공은 선택적 카탈로그 ID 번역 및 문자열 현지화를 적용합니다.

## 속성 {#section-1854a9902b884d9b8e8e713b6635723f}

요청 명령입니다. 지정된 위치에 관계없이 중첩된/포함된 요청을 포함한 전체 요청에 적용됩니다. `locId` 인쇄 가능한 ASCII 문자만 포함해야 합니다. 이 요청의 기본 카탈로그에 현지화 맵이 정의되지 않은 경우 무시됩니다. 비어 있거나 잘못된 경우 오류가 반환됩니다 `locId` 이(가) 지정되었으며 기본 규칙이 정의되지 않았습니다. `attribute::DefaultLocale`.

## 기본값 {#section-9699fbc26de6453e9029e0003c79a7ef}

`attribute::DefaultLocale` locale=을 지정하지 않은 경우 사용됩니다.

## 참조 {#section-28a586d43ac4429d98e318a580c92af4}

[attribute::DefaultLocale](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultlocale.md#reference-69462ad9923f464f80c2c012342a6b6b) , [attribute::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318), [attribute::LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e), 현지화 지원
