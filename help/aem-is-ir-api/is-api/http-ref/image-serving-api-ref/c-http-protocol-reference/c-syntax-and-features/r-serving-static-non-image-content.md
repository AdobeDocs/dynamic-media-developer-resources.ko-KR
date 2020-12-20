---
description: 널
seo-description: 널
seo-title: 정적(이미지가 아님) 컨텐츠 제공
solution: Experience Manager
title: 정적(이미지가 아님) 컨텐츠 제공
topic: Scene7 Image Serving - Image Rendering API
uuid: 4ec483fe-68a4-4ae2-b5ce-730229a9bc15
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 2%

---


# 정적(이미지가 아님) 컨텐츠 제공{#serving-static-non-image-content}

이미지 제공은 카탈로그에서 이미지가 아닌 컨텐츠를 관리하고 별도의 `context /is/content`을 통해 제공하는 메커니즘을 제공합니다. 이 메커니즘을 통해 각 항목에 대한 TTL을 별도로 구성할 수 있습니다.

## 기본 구문 {#section-a986baaca8644d04bcd0ddf781ae916e}

<table id="simpletable_4A6249F0C40747339524323EB0831CE4"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 요청  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> http://  <span class="varname"> server  </span>/is/content[/  <span class="varname"> catalog  </span>/  <span class="varname"> item  </span>][? <span class="varname"> 수정자  </span>]  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address  </span>[: <span class="varname"> 포트  </span>]  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 카탈로그  </span> </span> </p> </td> 
  <td class="stentry"> <p>카탈로그 식별자. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> item  </span> </span> </p> </td> 
  <td class="stentry"> <p>정적 컨텐츠 항목 ID. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 수정자  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> command  </span>*[&amp;  <span class="varname"> 명령  </span>]  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> command  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName  </span>=  <span class="varname"> 값  </span> </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName  </span> </span> </p> </td> 
  <td class="stentry"> <p>지원되는 명령 이름 중 하나입니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
  <td class="stentry"> <p>명령 값. </p> </td> 
 </tr> 
</table>

## 명령 개요 {#section-61657a0141914053ab12038ad7e91500}

이미지 제공은 /is/content에서 다음 명령을 지원합니다.

<table id="simpletable_1D96BA1AB5394B3C9B91D46617AFC0FA"> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb" type="reference" format="dita" scope="local"> type </a> </td> 
  <td class="stentry"> <p>콘텐츠 유형 필터입니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" type="reference" format="dita" scope="local"> req  </a> </td> 
  <td class="stentry"> <p> <span class="codeph"> req=userdata  </span>,  <span class="codeph"> req=props  </span>및  <span class="codeph"> req=존재  </span> 자체입니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" type="reference" format="dita" scope="local"> 캐시  </a> </td> 
  <td class="stentry"> <p>클라이언트측 캐시를 사용하지 않도록 설정합니다. </p> </td> 
 </tr> 
</table>

## 정적 컨텐츠 카탈로그 {#section-b2b8f4860fe84e528493ed704c7c5141}

정적 컨텐츠 카탈로그는 이미지 카탈로그와 비슷하지만 데이터 필드를 거의 지원하지 않습니다.

<table id="table_3B111EC3AA1044FB9B659FD54BADDC39"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 속성/데이터</b> </th> 
   <th class="entry"> <b> 주의</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> 카탈로그::Id  </span> </p> </td> 
   <td> <p> 이 정적 컨텐츠 항목에 대한 카탈로그 레코드 식별자 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> 카탈로그::경로  </span> </p> </td> 
   <td> <p> 이 콘텐트 항목의 파일 경로 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> 카탈로그::만료  </span> </p> </td> 
   <td> <p> 이 콘텐트 항목의 TTL;attribute::Expiration은 지정되지 않았거나 비어 있으면 사용됩니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> 카탈로그::타임스탬프  </span> </p> </td> 
   <td> <p> 파일 수정 타임스탬프;attribute::CacheValidationPolicy를 사용하여 카탈로그 기반 유효성 검사를 활성화할 때 필요합니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> 카탈로그::UserData  </span> </p> </td> 
   <td> <p> 이 정적 컨텐츠 항목과 연결된 선택적 메타데이터;req=userdata를 사용하여 클라이언트에서 사용 가능 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> 카탈로그::UserType  </span> </p> </td> 
   <td> <p> 선택적 데이터 유형;type= 명령을 사용하여 정적 컨텐츠에 대한 요청을 필터링하는 데 사용할 수 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 정적 컨텐츠 필터링 {#section-896c37cf68bc446eb0766fb378898262}

이 메커니즘은 클라이언트가 자신의 요구에 맞는 컨텐츠만 수신할 수 있도록 해줍니다. 정적 컨텐츠에 적절한 `catalog::UserType`값에 태그가 지정되어 있다고 가정할 때 클라이언트는 `type=` 명령을 요청에 추가할 수 있습니다. 이미지 제공은 `type=` 명령과 함께 제공된 값을 `catalog::UserType` 값과 비교하고, 일치하지 않을 경우 부적절한 내용이 아닌 오류를 반환합니다.

## 참조 {#section-91c7b686aacf4d3ca974f35a3fe3d6ec}

[type=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb) ,  [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76),  [이미지 카탈로그 참조](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)
