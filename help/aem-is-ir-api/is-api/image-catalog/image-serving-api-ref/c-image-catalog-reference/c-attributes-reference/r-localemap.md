---
description: ID 번역 맵. 일반 이미지 ID를 로케일별 ID로 변환하는 데 사용되는 규칙을 지정합니다.
solution: Experience Manager
title: 로케일 맵
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c1d74154-721b-46cc-9f0b-8dae5647b179
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 1%

---

# 로케일 맵{#localemap}

ID 번역 맵. 일반 이미지 ID를 로케일별 ID로 변환하는 데 사용되는 규칙을 지정합니다.

`*`항목`*&#42;['|' *`항목`*]`

<table id="simpletable_A6DD1A28F8ED4178A8ADDB2F3AEFC402"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 항목</span> </p></td> 
  <td class="stentry"> <p><span class="varname"> locId</span>,<span class="varname"> locSuffix</span>*[','<span class="varname"> locSuffix</span>] </p></td> 
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

`LocaleMap` 참조: `locId` 원하는 수에 매핑할 수 있음 `locSuffix`.

비어 있음 *`locSuffix`* 값을 사용할 수 있습니다. *`locSuffix`* 값은 검색할 순서대로 정렬해야 합니다. 첫 번째 일치 항목이 반환됩니다.

이미지 제공은 *`locId`* 대/소문자를 구분하지 않는 값을 `locale=` 요청에 지정된 값입니다. 일치하는 항목이 있으면 첫 번째 연결된 *`locSuffix`* 값이 원래 카탈로그 id에 추가됩니다. 이 카탈로그 항목이 있으면 사용되고, 그렇지 않으면 다음 항목이 사용됩니다. *`locSuffix`* 값을 시도했습니다. 다음 중 하나도 없는 경우 *`locSuffix`* 값이 카탈로그 항목과 일치하면 이미지 제공에서 오류 또는 기본 이미지를 반환합니다.

비어 있음 *`locId`* 값이 비어 있거나 알 수 없는 값과 일치함 `locale=` 문자열. 이를 통해 알 수 없는 로케일에 대한 기본 규칙을 정의할 수 있습니다.

활성화된 경우 ID 번역이 이미지 카탈로그 및 정적 콘텐츠 카탈로그 항목을 참조하는 모든 ID에 적용됩니다.

## 속성 {#section-f4c6f058bc5348ee9a3fb19e394b37e3}

다음으로 구분된 하나 이상의 항목 |: 각 항목은 둘 이상의 쉼표로 구분된 문자열 값으로 구성됩니다. *`locId`* 및 `locale=` 비교됩니다. 대/소문자를 구분하지 않습니다.

## 참조 {#section-19fba6d5be59439c8bf8ec7513c1a6da}

현지화 지원, [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [attribute::LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e)
