---
description: 이미지/메타데이터 버전. 자주 변경되는 컨텐츠로 작업할 때 Akamai, 브라우저 캐시 및 기업 프록시 서버 캐싱과 같은 캐싱 네트워크의 서버는 일정 기간 동안 최신 상태가 아닐 수 있는 이미지 제공 응답을 저장할 수 있습니다.
seo-description: 이미지/메타데이터 버전. 자주 변경되는 컨텐츠로 작업할 때 Akamai, 브라우저 캐시 및 기업 프록시 서버 캐싱과 같은 캐싱 네트워크의 서버는 일정 기간 동안 최신 상태가 아닐 수 있는 이미지 제공 응답을 저장할 수 있습니다.
seo-title: id
solution: Experience Manager
title: id
topic: Scene7 Image Serving - Image Rendering API
uuid: 3d526326-c8fa-4aef-95a9-93ccacf08f73
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 3%

---


# id{#id}

이미지/메타데이터 버전. 자주 변경되는 컨텐츠로 작업할 때 Akamai, 브라우저 캐시 및 기업 프록시 서버 캐싱과 같은 캐싱 네트워크의 서버는 일정 기간 동안 최신 상태가 아닐 수 있는 이미지 제공 응답을 저장할 수 있습니다.

` id= *`val`*`

<table id="simpletable_3A6EBDA15B004636804E1ACEF952479A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> val  </span> </span> </p> </td> 
  <td class="stentry"> <p>버전 문자열. </p> </td> 
 </tr> 
</table>

이미지 제공에는 오래된 캐시 항목을 응용 프로그램에서 사용할 수 있는 가능성을 줄이는 데 도움이 되는 버전 관리 메커니즘이 포함되어 있습니다. 이 메커니즘은 이미지 데이터 및 메타데이터(예: 이미지 맵 또는 확대/축소 대상 데이터)에 대한 버전 식별자 문자열을 얻기 위해 `req=props`을(를) 사용하는 것입니다. 그런 다음 버전 식별자 문자열이 `id=` 명령으로 캐시 가능한 이미지 제공 요청에 추가됩니다.

소스 이미지 또는 메타데이터가 변경되면 해당 버전 ID 값도 변경됩니다. `id=` 명령에 최신 버전 ID 값을 포함하면 이전 캐시 항목에 더 이상 액세스할 수 없습니다.

다음 표는 각 `req=` 유형에 사용할 버전 식별자 문자열을 보여 줍니다.

<table id="table_AE39BEBE18864880BBBF1C4F16785E2D"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> req= type</b> </th> 
   <th class="entry"> <b> req=prop의 버전 식별자</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> img </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 맵 </p> </td> 
   <td> <p> metadata.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 마스크 </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 목표 </p> </td> 
   <td> <p> metadata.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> tmb </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> userdata </p> </td> 
   <td> <p> metadata.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> xmp </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
 </tbody> 
</table>

`req=` 위에 나열되지 않은 유형에는 짧은 TTL(  `attribute::NonImgExpiration`)이 있거나 응답을 전혀 받을 수 없습니다.이러한 요청에 포함시키는 것 `id=` 은 장점이 없다.

## 속성 {#section-62e973d0d5884abebbb0679f9278ae2c}

요청 속성을 참조하십시오. 선택 사항입니다. 서버에서 항상 무시됩니다.

## 기본값 {#section-96136720c82842c89505347ec39e6024}

없음.

## 예 {#section-a5fb871e0ec8485c91c4fca78895d17f}

사용 예를 보려면 [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3)에 대한 설명을 참조하십시오.

## 참조 {#section-6b4befb47202415195a68516f60e9988}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) ,  [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3),  [카탈로그::만료](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a),  [속성::NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
