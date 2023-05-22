---
description: 정적(이미지가 아닌) 콘텐츠 제공
solution: Experience Manager
title: 정적(이미지가 아닌) 콘텐츠 제공
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e2c79bdc-5d70-46d9-85f4-ffebd7621944
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 1%

---

# 정적(이미지가 아닌) 콘텐츠 제공{#serving-static-non-image-content}

이미지 제공은 카탈로그의 비이미지 컨텐츠를 관리하고 별도의 메커니즘을 통해 제공하는 메커니즘을 제공합니다 `context /is/content`. 메커니즘을 통해 각 항목에 대한 TTL을 별도로 구성할 수 있습니다.

## 기본 구문 {#section-a986baaca8644d04bcd0ddf781ae916e}

<table id="simpletable_4A6249F0C40747339524323EB0831CE4"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 요청 </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> http:// <span class="varname"> server </span>/is/content[/ <span class="varname"> 카탈로그 </span>/ <span class="varname"> 항목 </span>][? <span class="varname"> 수정자 </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address </span>[: <span class="varname"> 포트 </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 카탈로그 </span> </span> </p> </td> 
  <td class="stentry"> <p>카탈로그 식별자. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 항목 </span> </span> </p> </td> 
  <td class="stentry"> <p>정적 콘텐츠 항목 ID. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 수정자 </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 명령 </span>*[&amp; <span class="varname"> 명령 </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 명령 </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName </span>= <span class="varname"> 값 </span> </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName </span> </span> </p> </td> 
  <td class="stentry"> <p>지원되는 명령 이름 중 하나입니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 값 </span> </span> </p> </td> 
  <td class="stentry"> <p>명령 값. </p> </td> 
 </tr> 
</table>

## 명령 개요 {#section-61657a0141914053ab12038ad7e91500}

이미지 제공은 /is/content에서 다음 명령을 지원합니다.

<table id="simpletable_1D96BA1AB5394B3C9B91D46617AFC0FA"> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb" type="reference" format="dita" scope="local"> type </a> </td> 
  <td class="stentry"> <p>콘텐츠 유형 필터. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" type="reference" format="dita" scope="local"> req </a> </td> 
  <td class="stentry"> <p> <span class="codeph"> req=userdata </span>, <span class="codeph"> req=props </span>, 및 <span class="codeph"> req=exists </span> 만 해당. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" type="reference" format="dita" scope="local"> 캐시 </a> </td> 
  <td class="stentry"> <p>클라이언트측 캐싱을 비활성화할 수 있습니다. </p> </td> 
 </tr> 
</table>

## 정적 콘텐츠 카탈로그 {#section-b2b8f4860fe84e528493ed704c7c5141}

정적 콘텐츠 카탈로그는 이미지 카탈로그와 유사하지만 더 적은 데이터 필드를 지원합니다.

<table id="table_3B111EC3AA1044FB9B659FD54BADDC39"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 속성/데이터</b> </th> 
   <th class="entry"> <b> 주의</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::Id </span> </p> </td> 
   <td> <p> 이 정적 콘텐츠 항목에 대한 카탈로그 레코드 식별자 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::Path </span> </p> </td> 
   <td> <p> 이 컨텐츠 항목의 파일 경로 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::Expiration </span> </p> </td> 
   <td> <p> 이 컨텐츠 항목의 TTL입니다. 지정되지 않았거나 비어 있는 경우 attribute::Expiration이 사용됩니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::TimeStamp </span> </p> </td> 
   <td> <p> 파일 수정 타임스탬프. 다음 속성으로 카탈로그 기반 유효성 검사를 활성화하는 경우 필요합니다.:CacheValidationPolicy </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::UserData </span> </p> </td> 
   <td> <p> 이 정적 콘텐츠 항목과 연결된 선택적 메타데이터입니다. req=userdata를 사용하여 클라이언트에서 사용할 수 있습니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::UserType </span> </p> </td> 
   <td> <p> 선택적 데이터 유형: type= 명령을 사용하여 정적 컨텐츠에 대한 요청을 필터링하는 데 사용할 수 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 정적 콘텐츠 필터링 {#section-896c37cf68bc446eb0766fb378898262}

이 메커니즘을 사용하면 클라이언트가 해당 요구 사항에 적합한 콘텐츠만 받도록 할 수 있습니다. 정적 컨텐츠에 적절한 태그가 지정되었다고 가정 `catalog::UserType`값을 지정하면 클라이언트가 `type=` 요청에 대한 명령입니다. 이미지 제공에서는 제공된 값을 `type=` 다음 값에 대한 명령: `catalog::UserType` 그리고 불일치가 발생하면 부적절한 콘텐츠 대신 오류를 반환합니다.

## 참조 {#section-91c7b686aacf4d3ca974f35a3fe3d6ec}

[type=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb) , [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [이미지 카탈로그 참조](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)
