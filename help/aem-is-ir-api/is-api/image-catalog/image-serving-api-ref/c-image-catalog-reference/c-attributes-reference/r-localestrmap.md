---
description: 문자열 번역 맵. 임의의 internalLocId에 매핑될 수 있는 locId를 나타냅니다.
solution: Experience Manager
title: LocaleStrMap
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 48a1c71c-78a9-43db-8b1a-4189d34b0982
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 1%

---

# LocaleStrMap{#localestrmap}

문자열 번역 맵. 임의의 internalLocId에 매핑될 수 있는 locId를 나타냅니다.

`*`항목`*&#42;['|' *`항목`*]`

<table id="simpletable_26A9A6904C85459F89DCDD98C14139CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 항목 </span> </p> </td> 
  <td class="stentry"> <p> <span class="varname"> 로케일 </span>, <span class="varname"> locId </span>*[',' <span class="varname"> locId </span>] </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 로케일 </span> </p> </td> 
  <td class="stentry"> <p>로케일(대/소문자 구분 안 함) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> locId </span> </p> </td> 
  <td class="stentry"> <p>내부 로케일 ID. </p> </td> 
 </tr> 
</table>

`LocaleStrMap` 참조: `locId` 원하는 수에 매핑할 수 있음 `internalLocId`.

비어 있음 *`locale`* 값이 비어 있거나 알 수 없는 값과 일치함 `locale=` 문자열. 이를 통해 알 수 없는 로케일에 대한 기본 규칙을 정의할 수 있습니다.

비어 있음 *`locId`* 값을 허용하고 다음을 선택합니다 *`defaultString`* (다음 *`defaultString`* 에는 로케일 식별자가 없습니다. *`locId`* 값은 지정된 순서대로 검색됩니다. 첫 번째 일치 항목이 반환됩니다.

문자열 변환이 활성화되면 다음 이미지 카탈로그 필드의 텍스트 문자열에 적용됩니다.

<table id="table_EE0321F9890B45CA8C364178F5100D40"> 
 <tbody> 
  <tr valign="top"> 
   <td> <b>카탈로그 필드</b> </td> 
   <td> <b>필드의 문자열 요소</b> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::ImageSet </span> </p> </td> 
   <td> <p>변환 가능한 문자열을 포함하는 모든 하위 요소(',' ';' ':' 및/또는 필드의 시작/끝 구분 기호의 조합으로 구분). </p> <p>A <span class="codeph"> 0xrrggbb </span> 현지화 가능 필드의 시작 부분에 있는 색상 값은 현지화에서 제외되며 수정 없이 전달됩니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::Map </span> </p> </td> 
   <td> <p>의 값을 제외한 모든 작은따옴표 또는 큰따옴표 속성 값 <span class="codeph"> 코드= </span> 및 <span class="codeph"> shape= </span> 속성. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::Target </span> </p> </td> 
   <td> <p>임의 값 <span class="filepath"> 타겟.*.label </span> 및 <span class="filepath"> 타겟.*.userdata </span> 속성. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::UserData </span> </p> </td> 
   <td> <p>모든 속성의 값입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-8505a8525f6948ada3979f68c4081044}

다음으로 구분된 하나 이상의 항목 |: 각 항목이 둘 이상의 쉼표로 구분된 문자열 값으로 구성됩니다.

## 참조 {#section-0c0516e4f83d42d38247308cab9b6708}

현지화 지원, [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [attribute::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318), [catalog::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md), [catalog::Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), [catalog::Target](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md), [catalog::UserData](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md)
