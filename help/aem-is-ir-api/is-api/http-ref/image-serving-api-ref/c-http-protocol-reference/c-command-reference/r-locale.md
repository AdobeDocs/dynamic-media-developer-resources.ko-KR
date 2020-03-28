---
description: 번역 로케일 ID. 요청에 대한 로케일 ID를 지정합니다.
seo-description: 번역 로케일 ID. 요청에 대한 로케일 ID를 지정합니다.
seo-title: 로케일
solution: Experience Manager
title: 로케일
topic: Scene7 Image Serving - Image Rendering API
uuid: 82acc0bb-fd94-44c9-8ff9-3b9cefab4627
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 로케일{#locale}

번역 로케일 ID. 요청에 대한 로케일 ID를 지정합니다.

`locale=[ *`locId`*]`

<table id="simpletable_C1899AD02C984ED3896B7620916637E7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> locId <span class="varname"></span></span> </p> </td> 
  <td class="stentry"> <p>로케일 ID(문자열). </p></td> 
 </tr> 
</table>

이미지 제공은 이 ID와 `attribute::LocaleMap` `attribute::LocaleStrMap`와 함께 지정된 규칙을 사용하여 선택적 카탈로그 ID 번역 및 문자열 현지화를 적용합니다.

## 속성 {#section-1854a9902b884d9b8e8e713b6635723f}

요청 명령. 지정된 위치에 관계없이 중첩된 요청/포함된 요청을 포함하여 전체 요청에 적용됩니다. `locId` 는 인쇄 가능한 ASCII 문자만 포함해야 합니다. 이 요청의 주 카탈로그에 정의된 현지화 맵이 없는 경우 무시됩니다. 비어 있거나 잘못된 규칙이 `locId` 지정되고 기본 규칙이 정의되지 않은 경우 오류가 반환됩니다 `attribute::DefaultLocale`.

## 기본값 {#section-9699fbc26de6453e9029e0003c79a7ef}

`attribute::DefaultLocale` 는 locale=가 지정되지 않은 경우에 사용됩니다.

## 참조 {#section-28a586d43ac4429d98e318a580c92af4}

[attribute::DefaultLocale](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultlocale.md#reference-69462ad9923f464f80c2c012342a6b6b) , [attribute::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318), [속성::LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e), 현지화 지원
