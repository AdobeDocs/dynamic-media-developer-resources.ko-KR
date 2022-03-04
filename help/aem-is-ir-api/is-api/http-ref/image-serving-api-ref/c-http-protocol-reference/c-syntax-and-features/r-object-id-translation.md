---
description: 이미지 제공 기능은 외부 개체 ID를 로케일 특정 개체(카탈로그) ID로 변환하는 메커니즘을 제공합니다. 기본 응용 프로그램은 로케일 특정 개체 ID를 알 필요가 없는 클라이언트 응용 프로그램이 여러 로케일 간에 공유되는 컨텐츠와 로케일 특정 컨텐츠를 제공하는 것입니다.
solution: Experience Manager
title: 개체 ID 번역
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7a3bd6a1-2ad4-4da2-944c-489b7d18fdc1
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '696'
ht-degree: 9%

---

# 개체 ID 번역{#object-id-translation}

이미지 제공 기능은 외부 개체 ID를 로케일 특정 개체(카탈로그) ID로 변환하는 메커니즘을 제공합니다. 기본 응용 프로그램은 로케일 특정 개체 ID를 알 필요가 없는 클라이언트 응용 프로그램이 여러 로케일 간에 공유되는 컨텐츠와 로케일 특정 컨텐츠를 제공하는 것입니다.

글로벌 개체 ID만 사용하여 응용 프로그램을 작성할 수 있으며, 이미지 제공 기능은 로케일 특정 이미지와 사용 가능한 다른 콘텐츠를 자동으로 대체하게 됩니다.

다음 *`locale`* 는 `locale=` 명령.

>[!NOTE]
>
>개체 ID 변환은 이미지 제공 카탈로그 기반 사용에만 적용할 수 있습니다. 파일 이름을 변환할 수 없습니다.

## 범위 {#section-66fcd5bd467c4eeaa1574583cbe9756d}

이미지, SVG 및 정적 컨텐츠 카탈로그의 항목에 대한 모든 참조는 번역 글꼴로 간주되며 ICC 프로필 참조는 번역되지 않습니다. 추가 *`object`* 의 경로 [!DNL /is/image] 및 [!DNL /is/static requests], 이러한 명령 및 카탈로그 속성은 ID 번역을 따릅니다. `src=`, `mask=`, `template=`, `defaultImage=`, `attribute::DefaultImage`, 및 `attribute::Watermark`.

## ID 번역 맵 {#section-9e417b352c314dfe94e831fdd62cddc8}

`attribute::LocaleMap` 는 일반 개체 ID 및 `locale=` 값.

`attribute::LocaleMap` 입력 목록으로 구성됩니다 *로케일* (에 지정된 값 일치 `locale=`), 출력 로케일 접미사가 없는 각 항목( `*`locSuffixes`*`).

예, `attribute::LocaleMap` 다음과 같습니다.

`en,_E,|en_us,_E,|en_uk,_E,|fr,_F,|de,_D,|de_at,_D,|de_de,_D,|,_E,`

요청 `/is/image/myCat/myImg?locale=de_de` 카탈로그 항목과 연결된 이미지를 반환합니다. `myCat/myImg_D` (이러한 카탈로그 항목이 있다고 가정함)

의 설명을 참조하십시오. `attribute::LocaleMap` 자세한 내용

## 번역 프로세스 {#section-1f64db17e9f644d88e09853670e14a16}

위의 예에서 서버가 먼저 *`locale`* &quot; `de_de`&quot;(ID 변환 맵)의. 그런 다음 를 반복합니다 *`locSuffixes`* 이 경우 &quot; `_D`&quot; 및 &quot;&quot;(빈 접미어). 각 반복에 대해 접미사는 이미지 ID에 추가되고 카탈로그에 있는지 테스트된 결과 ID에 추가됩니다. 찾은 경우 해당 카탈로그 항목이 사용되고 그렇지 않은 경우에는 다음 항목이 테스트됩니다. 이 예제에서는 다음 항목을 선택합니다. `myCat/myImg_D`, 및 `myCat/myImg`. 일치하는 항목이 없으면 서버에서 오류 또는 기본 이미지(구성된 경우)를 반환합니다.

## 알 수 없는 로케일 {#section-b2f3c83f2dc845d69b5908107b775537}

위의 예에서 `attribute::LocaleMap` 빈 포함 *`locale`* 알 수 없음에 사용되는 기본 번역 규칙을 정의하는 것입니다 `locale=` 값(즉, 번역 맵에 명시적으로 나열되지 않은 값). 이 번역 맵이 요청에 적용된 경우 `/is/image/myCat/myImg?locale=ja`로 설정되면 `myCat/myImg_E`, 있는 경우 또는 없는 경우 `myCat/myImg`.

번역 맵에서 기본 번역 규칙을 지정하지 않으면 알 수 없는 모든 요청에 대해 오류가 반환됩니다 `locale=` 값.

## 예제 {#section-cc40bb00ee9248bb8cb23e17d7a5984c}

**다중 계층 조회**

지역 표준을 해결하기 위해 종종 로케일(예: 유럽, 중동, 북미)을 그룹화하는 것이 좋습니다. 이 작업은 다중 계층 조회를 사용하여 수행할 수 있습니다.

이 예에서는 서양 및 중동 사용자를 위한 컬렉션을 지원하려고 합니다. 두 컬렉션은 모두 일반 이미지 컬렉션을 기반으로 하며, 모두 여러 이미지를 추가하거나 수정합니다. 그런 다음 두 컬렉션을 특정 로케일( `m1`, `m2` 2개의 중동 변형에 대해, `w1`, `w2`, 및 `w3` 이미지가 공유되는 경우를 제외하고 세 개의 서양 로케일의 경우) `w1` 및 `w3`. 알 수 없는 로케일은 일반 컬렉션에만 매핑되고, 로케일별 이미지에는 액세스하지 못했습니다.

`attribute::LocaleMap: w1,-W,|w2,-W2,-W,|w3,-W,|m1,-M1,-M,|m2,-M2,-M,|,`

다음 표는 고려되는 카탈로그 항목과 일반 입력 ID에 대해 고려되는 순서를 보여줍니다 `myImg`:

<table id="table_97EB13E3DB9B48D3A4184D5ECC8E9F86"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>로케일</i> </b> </th> 
   <th class="entry"> <b>검색할 카탈로그 ID</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> w1, w3 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-W, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> w2 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-W2, myImg-W, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> m1 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-M1, myImg-M, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> m2 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-M2, myImg-M, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>기타 </p> </td> 
   <td> <p> <span class="codeph"> myImg </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

**특정 ID 검색**

일부 이미지 이름 지정 규칙은 내부적으로 일반 이미지 ID를 지원하지 않을 수 있습니다. 요청의 일반 ID는 항상 카탈로그의 특정 ID에 매핑되어야 합니다. 종종 정확한 특정 ID를 알 수 없을 수 있습니다.

이 예에서는 모든 언어에 대한 이미지에 `_1`, `_2`, 또는 `_3` 접미사. 프랑스어 로켈에 대한 이미지에는 `_22` 또는 `_23` 접미사 및 독일어 로케일에 대한 이미지에는 `_470` 또는 `_480` 접미사.

`attribute::LocaleMap: ,_1,_2,_3|fr,_22,_23,_1,_2,_3|de,_470,_480,_1,_2,_3| de_at,_470,_480,_1,_2,_3| de_de,_470,_480,_1,_2,_3`

다음 표는 고려되는 카탈로그 항목과 일반 입력 ID에 대해 고려되는 순서를 보여줍니다 `myImg`:

<table id="table_A7EE4AA0F1C24284B83CC4B40622D24F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>로케일</i> </b> </th> 
   <th class="entry"> <b>검색할 출력 ID</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> fr </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg_22, myImg_23, myImg_1, myImg_2,myImg_3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> de </span>, <span class="codeph"> de_at </span>, <span class="codeph"> de_de </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg_470, myImg_480, myImg_1, myImg_2,myImg_3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>기타 </p> </td> 
   <td> <p> <span class="codeph"> myImg_1, myImg_2, myImg_3 </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 참조 {#section-05893816c66a406d89f9bfd6ace8d47a}

[속성::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318) , [attribute::DefaultLocale](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultlocale.md#reference-69462ad9923f464f80c2c012342a6b6b), [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [req=xlate](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
