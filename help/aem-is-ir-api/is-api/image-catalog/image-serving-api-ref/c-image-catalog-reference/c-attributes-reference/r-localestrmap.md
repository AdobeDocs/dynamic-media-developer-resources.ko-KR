---
description: 문자열 번역 맵. 임의 개수의 internalLocId에 매핑할 수 있는 locId를 참조합니다.
seo-description: 문자열 번역 맵. 임의 개수의 internalLocId에 매핑할 수 있는 locId를 참조합니다.
seo-title: LocaleStrMap
solution: Experience Manager
title: LocaleStrMap
topic: Scene7 Image Serving - Image Rendering API
uuid: 44207916-80a6-42cb-8bf1-fcf0f5194c6d
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 1%

---


# LocaleStrMap{#localestrmap}

문자열 번역 맵. 임의 개수의 internalLocId에 매핑할 수 있는 locId를 참조합니다.

` *``*&#42;['|' *`항목`*]`

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

`LocaleStrMap` 은  `locId` 수에 관계없이 매핑할 수 있는 항목을  `internalLocId`나타냅니다.

빈 *`locale`* 값은 비어 있고 알 수 없는 `locale=` 문자열을 찾습니다. 알 수 없는 로케일에 대한 기본 규칙을 정의할 수 있습니다.

빈 *`locId`* 값이 허용되고 *`defaultString`*(*`defaultString`*&#x200B;에 로케일 식별자가 없음)을 선택합니다. *`locId`* 값이 지정된 순서로 검색됩니다. 첫 번째 일치 항목이 반환됩니다.

문자열 변환은 활성화되면 다음 이미지 카탈로그 필드의 텍스트 문자열에 적용됩니다.

<table id="table_EE0321F9890B45CA8C364178F5100D40"> 
 <tbody> 
  <tr valign="top"> 
   <td> <b>카탈로그 필드</b> </td> 
   <td> <b>필드의 문자열 요소</b> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> 카탈로그::ImageSet  </span> </p> </td> 
   <td> <p>번역 가능한 문자열이 포함된 하위 요소(구분 기호 ',' ';' ':' 및/또는 필드의 시작/끝 조합으로 구분). </p> <p>지역화 가능 필드의 시작 부분에 있는 <span class="codeph"> 0xrggbb </span> 색상 값은 로컬라이제이션에서 제외되고 수정 없이 전달됩니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> 카탈로그::맵  </span> </p> </td> 
   <td> <p><span class="codeph"> coords= </span> 및 <span class="codeph"> shape= </span> 속성의 값을 제외한 모든 단일 또는 이중 인용 특성 값입니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> 카탈로그::Target  </span> </p> </td> 
   <td> <p><span class="filepath"> 대상의 값입니다.*.label </span> 및 <span class="filepath"> target.*.userdata </span> 속성. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> 카탈로그::UserData  </span> </p> </td> 
   <td> <p>모든 속성의 값입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-8505a8525f6948ada3979f68c4081044}

하나 이상의 항목이 |. 여기서 각 항목은 두 개 이상의 쉼표로 구분된 문자열 값으로 구성됩니다.

## 참조 {#section-0c0516e4f83d42d38247308cab9b6708}

현지화 지원, [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [속성::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318), [카탈로그::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md), [카탈로그::Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), [카탈로그::Target](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md), [카탈로그: userData](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md)
