---
description: 문자열 번역 맵. 임의의 internalLocId에 매핑할 수 있는 locId를 참조합니다.
solution: Experience Manager
title: LocaleStrMap
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 48a1c71c-78a9-43db-8b1a-4189d34b0982
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 2%

---

# LocaleStrMap{#localestrmap}

문자열 번역 맵. 임의의 internalLocId에 매핑할 수 있는 locId를 참조합니다.

`*``*&#42;['|' *`항목`*]`

<table id="simpletable_26A9A6904C85459F89DCDD98C14139CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 항목 </span> </p> </td> 
  <td class="stentry"> <p> <span class="varname"> locale  </span>,  <span class="varname"> locId  </span>*[','  <span class="varname"> locId  </span>] </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 로케일 </span> </p> </td> 
  <td class="stentry"> <p>로케일(대/소문자 구분 안 함). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> locId  </span> </p> </td> 
  <td class="stentry"> <p>내부 로케일 ID. </p> </td> 
 </tr> 
</table>

`LocaleStrMap` 는  `locId` 수에 관계없이 매핑할 수 있는 를  `internalLocId`나타냅니다.

빈 *`locale`* 값은 비어 있고 알 수 없는 `locale=` 문자열과 일치합니다. 알 수 없는 로케일에 대한 기본 규칙을 정의할 수 있습니다.

빈 *`locId`* 값이 허용되며 *`defaultString`*(*`defaultString`*&#x200B;에 로케일 식별자가 없음)을 선택합니다. *`locId`* 지정한 순서대로 값이 검색됩니다. 첫 번째 일치 항목이 반환됩니다.

문자열 번역이 활성화되면 다음 이미지 카탈로그 필드의 텍스트 문자열에 적용됩니다.

<table id="table_EE0321F9890B45CA8C364178F5100D40"> 
 <tbody> 
  <tr valign="top"> 
   <td> <b>카탈로그 필드</b> </td> 
   <td> <b>필드의 문자열 요소</b> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> 카탈로그::ImageSet  </span> </p> </td> 
   <td> <p>번역 가능한 문자열(',' ';' ':' 및/또는 필드의 시작/끝의 조합으로 구분)이 포함된 모든 하위 요소. </p> <p>지역화 가능한 필드의 시작 부분에 있는 <span class="codeph"> 0xrggbb </span> 색상 값이 지역화에서 제외되고 수정 없이 전달됩니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> 카탈로그::맵  </span> </p> </td> 
   <td> <p><span class="codeph"> coords= </span> 및 <span class="codeph"> shape= </span> 속성 값을 제외한 모든 단일 또는 이중 따옴표 속성 값 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> 카탈로그::Target  </span> </p> </td> 
   <td> <p><span class="filepath"> 대상의 값입니다.*.label </span> 및 <span class="filepath"> target.*.userdata </span> 속성을 사용합니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> 카탈로그::UserData  </span> </p> </td> 
   <td> <p>모든 속성의 값입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-8505a8525f6948ada3979f68c4081044}

하나 이상의 항목, |, 여기서 각 항목은 두 개 이상의 쉼표로 구분된 문자열 값으로 구성됩니다.

## 참조 {#section-0c0516e4f83d42d38247308cab9b6708}

로컬라이제이션 지원, [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [특성::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318), [catalog::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md), [catalog::Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), [카탈로그::Target](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md), [카탈로그::UserData](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md)
