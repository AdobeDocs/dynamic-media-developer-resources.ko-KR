---
description: 문자열 번역 맵. 임의의 internalLocId에 매핑될 수 있는 locId를 나타냅니다.
solution: Experience Manager
title: LocaleStrMap
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 48a1c71c-78a9-43db-8b1a-4189d34b0982
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---

# LocaleStrMap{#localestrmap}

문자열 번역 맵. 임의의 internalLocId에 매핑될 수 있는 locId를 나타냅니다.

`*`항목`*&#42;['|' *`항목`*]`

<table id="simpletable_26A9A6904C85459F89DCDD98C14139CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname">개 항목 </span> </p> </td> 
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

`LocaleStrMap`은(는) `locId` 수에 매핑할 수 있는 `internalLocId`을(를) 참조합니다.

빈 *`locale`* 값은 빈 문자열 및 알 수 없는 `locale=` 문자열과 일치합니다. 이를 통해 알 수 없는 로케일에 대한 기본 규칙을 정의할 수 있습니다.

빈 *`locId`* 값이 허용되고 *`defaultString`*&#x200B;을(를) 선택합니다(*`defaultString`*&#x200B;에 로케일 식별자가 없음). *`locId`*&#x200B;개의 값이 지정된 순서대로 검색됩니다. 첫 번째 일치 항목이 반환됩니다.

문자열 변환이 활성화되면 다음 이미지 카탈로그 필드의 텍스트 문자열에 적용됩니다.

<table id="table_EE0321F9890B45CA8C364178F5100D40"> 
 <tbody> 
  <tr valign="top"> 
   <td> <b>카탈로그 필드</b> </td> 
   <td> <b>필드의 문자열 요소</b> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> 카탈로그::ImageSet </span> </p> </td> 
   <td> <p>변환 가능한 문자열을 포함하는 모든 하위 요소(',' ';' ':' 및/또는 필드의 시작/끝 구분 기호의 조합으로 구분). </p> <p>지역화할 수 있는 필드의 시작 부분에 있는 <span class="codeph"> 0xrrggbb </span> 색 값이 지역화에서 제외되며 수정 없이 통과됩니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> 카탈로그::맵 </span> </p> </td> 
   <td> <p><span class="codeph"> 코드= </span> 및 <span class="codeph"> 셰이프= </span> 특성의 값을 제외한 모든 작은따옴표 또는 큰따옴표 특성 값입니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> 카탈로그::대상 </span> </p> </td> 
   <td> <p><span class="filepath"> 대상의 값입니다.*.label </span> 및 <span class="filepath"> 대상.*.userdata </span> 속성입니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> 카탈로그::UserData </span> </p> </td> 
   <td> <p>모든 속성의 값입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-8505a8525f6948ada3979f68c4081044}

다음으로 구분된 하나 이상의 항목 |: 각 항목이 둘 이상의 쉼표로 구분된 문자열 값으로 구성됩니다.

## 참조 {#section-0c0516e4f83d42d38247308cab9b6708}

현지화 지원, [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [attribute::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318), [catalog::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md), [catalog::Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), [catalog::Targets](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md), [catalog::UserData](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md)
