---
description: 이미지 제공을 사용하여 카탈로그의 비이미지 컨텐츠를 관리하고 별도의 /is/content 컨텍스트를 통해 제공할 수 있습니다.
seo-description: 이미지 제공을 사용하여 카탈로그의 비이미지 컨텐츠를 관리하고 별도의 /is/content 컨텍스트를 통해 제공할 수 있습니다.
seo-title: 정적(이미지가 아님) 컨텐츠 제공
solution: Experience Manager
title: 정적(이미지가 아님) 컨텐츠 제공
topic: Scene7 Image Serving - Image Rendering API
uuid: bdb1383a-e02d-499f-be79-4a6dc501705c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 정적(이미지가 아님) 컨텐츠 제공{#serving-static-non-image-contents}

이미지 제공을 사용하여 카탈로그의 비이미지 컨텐츠를 관리하고 별도의 /is/content 컨텍스트를 통해 제공할 수 있습니다.

이 기능을 사용하면 각 항목에 대한 TTL을 별도로 구성할 수 있습니다.

Image Serving은 에서 다음 명령을 지원합니다. [!DNL /is/content]:

<table id="simpletable_8A3AB1D1D20F4B6CBE86767E94735980"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb" format="dita" scope="local"> type </a> </p> </td> 
  <td class="stentry"> <p>콘텐츠 유형 필터. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" format="dita" scope="local"> req </a> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> req=userdata </span>, <span class="codeph"> req=props </span>및 <span class="codeph"> req=exists </span> 만 있습니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" format="dita" scope="local"> 캐시 </a> </p> </td> 
  <td class="stentry"> <p>클라이언트측 캐시를 비활성화할 수 있습니다. </p> </td> 
 </tr> 
</table>

## 기본 구문 {#section-42103439011540b2b9da3b5eebb442cd}

<table id="simpletable_2F039A5BFA2C4E22B014F42ECBCDA0A2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 요청 </span></span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> http:// <span class="filepath"> 서버 <span class="varname"> /is/content[/catalog/ </span>item <span class="varname"> </span>][? <span class="varname"> 수정자 </span>] </span></span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 서버 </span></span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address </span>[ : <span class="varname"> 포트 </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 카탈로그 </span></span> </p> </td> 
  <td class="stentry"> <p>카탈로그 식별자입니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 항목 </span></span> </p> </td> 
  <td class="stentry"> <p>정적 컨텐츠 항목 ID. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 수정자 </span></span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 명령 </span>*[&amp; <span class="varname"> command </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 명령 </span></span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName </span>= <span class="varname"> value </span></span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> cmd <span class="varname"> 이름 </span></span> </p> </td> 
  <td class="stentry"> <p>지원되는 명령 이름 중 하나입니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 값 </span></span> </p> </td> 
  <td class="stentry"> <p>명령 값. </p> </td> 
 </tr> 
</table>

## 정적 컨텐츠 카탈로그 {#section-91014f17f0d543d7aaf24539b2d7d4b9}

정적 컨텐츠 카탈로그는 이미지 카탈로그와 비슷하지만 데이터 필드 수를 지원합니다.

<table id="table_71A565DF5EC94913AD35CB13B0C7A27D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>속성/데이터 </p> </th> 
   <th colname="col2" class="entry"> <p>주의 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 카탈로그::Id </span> </p> </td> 
   <td colname="col2"> <p>이 정적 콘텐츠 항목의 카탈로그 레코드 식별자입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 카탈로그::경로 </span> </p> </td> 
   <td colname="col2"> <p>이 콘텐트 항목의 파일 경로입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 카탈로그::만료 </span> </p> </td> 
   <td colname="col2"> <p>이 콘텐트 항목의 TTLattribute::Expiration <span class="codeph"> </span> 은 지정하지 않았거나 비어 있는 경우 사용됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 카탈로그::타임스탬프 </span> </p> </td> 
   <td colname="col2"> <p>파일 수정 타임스탬프;attribute::CacheValidationPolicy를 사용하여 카탈로그 기반 유효성 검사를 활성화한 경우 <span class="codeph"> 필요합니다 </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 카탈로그::UserData </span> </p> </td> 
   <td colname="col2"> <p>이 정적 컨텐츠 항목과 연결된 선택적 메타데이터;req=userdata를 사용하여 클라이언트에 <span class="codeph"> 사용할 수 </span>있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::UserType </span> </p> </td> 
   <td colname="col2"> <p>선택적 데이터 유형;를 사용하여 <span class="codeph"> type= 명령을 사용하여 정적 컨텐트에 대한 요청을 필터링할 수 </span>있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 정적 컨텐츠 필터링 {#section-4c41bf41ff994910840c1352683d1f37}

이 메커니즘은 클라이언트가 요구 사항에 적합한 컨텐츠만 수신할 수 있도록 해줍니다. 정적 컨텐츠에 적절한 `catalog::UserType` 값이 태그로 지정되어 있다고 가정할 때 클라이언트는 `type=` 명령을 요청에 추가할 수 있습니다. 이미지 제공은 `type=` 명령과 함께 제공된 값을 의 값과 `catalog::UserType` 비교하고, 일치하지 않는 경우 부적절한 내용이 아닌 오류를 반환합니다.

## 비디오 캡션 파일 {#section-1ad25e10399e43eaa8ecb09b531dbf1a}

비디오 캡션 파일(WebVTT), CSS 또는 모든 텍스트 파일을 JSONP 형식으로 캡슐화할 수 있습니다. JSON 응답은 아래에 설명되어 있습니다.

* WebVTT 파일의 경우 응답의 MIME 유형은 text/javascript입니다. JSON이 반환되지 않음;대신 JSON을 사용하는 메서드를 호출하는 Javascript가 반환됩니다. ID와 핸들러는 모두 선택 사항입니다.
* CSS 파일의 경우 응답의 MIME 유형은 text/javascript입니다. ID와 핸들러는 모두 선택 사항입니다.
* 기본적으로 UTF-8 인코딩은 디코딩이 올바르게 수행되도록 적용됩니다. 기본 크기 제한은 2MB입니다.

다른 유형의 시간 메타데이터에 대한 트랙을 사용할 수도 있습니다. 각 트랙 요소의 소스 데이터는 시간 큐 목록으로 구성된 텍스트 파일입니다. 큐에는 JSON 또는 CSV와 같은 형식의 데이터를 포함할 수 있습니다.

JSONP [포맷에](http://en.wikipedia.org/wiki/JSONP) 대한 자세한 내용은 http://en.wikipedia.org/wiki/JSONP을 참조하십시오.

JSON [포맷에](http://www.json.org) 대한 자세한 내용은 www.json.org을 참조하십시오.

## 참조 {#section-7b28631016044a22a3a6762fd64771e9}

[type=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb) , [req=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [이미지 카탈로그 참조](../../is-api/image-serving-api-ref/c-image-catalog-reference/c-image-catalog-reference.md#concept-e23d45ea3abe43119d5144e01c14b0b5)
