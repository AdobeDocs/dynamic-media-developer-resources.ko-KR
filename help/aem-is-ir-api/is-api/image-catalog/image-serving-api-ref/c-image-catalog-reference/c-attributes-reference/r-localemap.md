---
description: ID 번역 맵. 일반 이미지 ID를 로케일 특정 ID로 변환하는 데 사용되는 규칙을 지정합니다.
solution: Experience Manager
title: LocaleMap
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: c1d74154-721b-46cc-9f0b-8dae5647b179
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 1%

---

# LocaleMap{#localemap}

ID 번역 맵. 일반 이미지 ID를 로케일 특정 ID로 변환하는 데 사용되는 규칙을 지정합니다.

`*``*&#42;['|' *`항목`*]`

<table id="simpletable_A6DD1A28F8ED4178A8ADDB2F3AEFC402"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 항목</span> </p></td> 
  <td class="stentry"> <p><span class="varname"> locId</span>, <span class="varname"> locSuffix</span>*[','<span class="varname"> locSuffix</span>] </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> locId</span> </p></td> 
  <td class="stentry"> <p>로케일 ID(대/소문자 구분 안 함). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> locSuffix</span> </p></td> 
  <td class="stentry"> <p>로케일 접미사. </p></td> 
 </tr> 
</table>

`LocaleMap` 는  `locId` 수에 관계없이 매핑할 수 있는 를  `locSuffix`나타냅니다.

빈 *`locSuffix`* 값이 허용됩니다. *`locSuffix`* 값을 검색할 순서대로 정렬해야 합니다. 첫 번째 일치 항목이 반환됩니다.

이미지 제공은 *`locId`* 값을 검색하여 요청에 지정된 `locale=` 값과 대/소문자를 구분하지 않는 일치를 검색합니다. 일치하는 항목이 있으면 연결된 첫 번째 *`locSuffix`* 값이 원래 카탈로그 ID에 추가됩니다. 이 카탈로그 항목이 있으면 사용합니다. 그렇지 않으면 다음 *`locSuffix`* 값이 시도됩니다. *`locSuffix`* 값 중 어느 하나도 카탈로그 항목과 일치하지 않으면 이미지 제공 시 오류 또는 기본 이미지가 반환됩니다.

빈 *`locId`* 값은 비어 있고 알 수 없는 `locale=` 문자열과 일치합니다. 알 수 없는 로케일에 대한 기본 규칙을 정의할 수 있습니다.

ID 변환은 활성화되면 이미지 카탈로그 및 정적 컨텐츠 카탈로그 항목을 참조하는 모든 ID에 적용됩니다.

## 속성 {#section-f4c6f058bc5348ee9a3fb19e394b37e3}

하나 이상의 항목, |, 여기서 각 항목은 두 개 이상의 쉼표로 구분된 문자열 값으로 구성됩니다. *`locId`* 와  `locale=` 비교됩니다. 대/소문자를 구분하지 않습니다.

## 참조 {#section-19fba6d5be59439c8bf8ec7513c1a6da}

지역화 지원, [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [특성::LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e)
