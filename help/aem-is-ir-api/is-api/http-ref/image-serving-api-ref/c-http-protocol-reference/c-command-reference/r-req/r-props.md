---
description: 응답 데이터 속성. 현재 요청을 이미지 요청(req=img)인 것처럼 평가하지만, 이미지를 반환하는 대신 서버는 응답 이미지의 선택된 속성을 반환합니다.
solution: Experience Manager
title: props
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9933d1dc-ae16-4d17-80ca-a1068cd73b0c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 5%

---

# props{#props}

응답 데이터 속성. 현재 요청을 이미지 요청(req=img)인 것처럼 평가하지만, 이미지를 반환하는 대신 서버는 응답 이미지의 선택된 속성을 반환합니다.

` req=props[,text|javascript|xml|{json[&id= *`reqId`*}]`

<table id="simpletable_A9FCC880171B4A9DBAE28413AFDF75F7"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> reqId </span> </span> </p> </td> 
  <td class="stentry"> <p>고유 요청 식별자. </p> </td> 
 </tr> 
</table>

JSONP 응답 형식을 지원하는 요청을 사용하면 `req=` 매개 변수의 확장 구문을 사용하여 JS 콜백 처리기의 이름을 지정할 수 있습니다.

`req=...,json [&handler = reqHandler ]`

`<reqHandler>`은(는) JSONP 응답에 있는 JS 처리기의 이름입니다. a-z, A-Z 및 0~9자만 허용됩니다. 선택 사항입니다. 기본값은 `s7jsonResponse`입니다.

응답 구문 및 응답 MIME 유형에 대한 설명은 [속성](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9)을 참조하십시오. HTTP 응답은 `attribute::NonImgExpiration`을(를) 기반으로 하는 TTL로 캐시할 수 있습니다.

/is/image 요청에 대해 다음 속성이 반환됩니다.

<table id="table_9665612ED7D24C07AAF75D953C0FEB36"> 
 <tbody> 
  <tr> 
   <td> <b> 속성</b> </td> 
   <td> <b> 유형</b> </td> 
   <td> <b> 설명</b> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.bgc </span> </p> </td> 
   <td> <p> 16 </p> </td> 
   <td> <p> 배경색(<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88" type="reference" format="dita" scope="local"> bgc= </a> </span> 참조) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td valign="top"> <p> <span class="codeph"> image.height </span> </p> </td> 
   <td> <p> 정수 </p> </td> 
   <td> <p> 응답 이미지 높이(픽셀) </p> </td> 
  </tr> 
  <tr> 
   <td valign="top"> <p> <span class="codeph"> image.iccEmbed </span> </p> </td> 
   <td> <p> 부울 </p> </td> 
   <td> <p> ICC 프로파일이 응답 이미지에 포함되어 있으면 True입니다. (<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e" type="reference" format="dita" scope="local"> IccEmbed= </a> </span> 참조) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.iccProfile </span> </p> </td> 
   <td> <p> 문자열 </p> </td> 
   <td> <p> 응답 이미지와 연결된 프로필의 이름/설명입니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.length </span> </p> </td> 
   <td> <p> 정수 </p> </td> 
   <td> <p> HTTP 헤더를 포함하지 않는 픽셀 단위의 응답 크기. 서버에서 이전에 응답 이미지 데이터가 캐시되지 않은 경우 0입니다. <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" type="reference" format="dita" scope="local"> req=loadcache </a> </span>을(를) 참조하십시오. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.mask </span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> 응답 이미지에 알파 채널이 포함된 경우 1, 그렇지 않은 경우 0입니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.pixType </span> </p> </td> 
   <td> <p> 문자열 </p> </td> 
   <td> <p> 응답 이미지 형식에는 <span class="codeph"> CMYK </span>, <span class="codeph"> RGB </span> 또는 <span class="codeph"> BW </span>(회색 음영 이미지의 경우)가 있습니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.pathEmbed </span> </p> </td> 
   <td> <p> 부울 </p> </td> 
   <td> <p> 응답 이미지가 경로를 임베드하는 경우 1, 그렇지 않은 경우 0. <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pathembed.md#reference-9ccf0771d6634cf68c1c9c33cd428301" type="reference" format="dita" scope="local"> pathEmbed= </a> </span>을(를) 참조하십시오. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.printRes </span> </p> </td> 
   <td> <p> 실제 </p> </td> 
   <td> <p> 인쇄 해상도(dpi) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.quality </span> </p> </td> 
   <td> <p> 정수 </p> </td> 
   <td> <p> JPEG 품질. (<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352" type="reference" format="dita" scope="local"> qlt= </a> </span> 참조) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.type </span> </p> </td> 
   <td> <p> 문자열 </p> </td> 
   <td> <p> 응답 이미지에 대한 MIME 유형입니다. (<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a" type="reference" format="dita" scope="local"> fmt= </a> </span> 참조) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.width </span> </p> </td> 
   <td> <p> 정수 </p> </td> 
   <td> <p> 응답 이미지 너비(픽셀 단위). </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.xmpEmbed </span> </p> </td> 
   <td> <p> 부울 </p> </td> 
   <td> <p> 응답 이미지가 xmp 데이터를 임베드하면 1, 그렇지 않으면 0이 됩니다. (<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-xmpembed.md#reference-46ecf40a40a0442fa62de3a85dcb03e8" type="reference" format="dita" scope="local"> xmpEmbed= </a> </span> 참조) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.version </span> </p> </td> 
   <td> <p> 문자열 </p> </td> 
   <td> <p> 이미지 버전 식별자. (<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0" type="reference" format="dita" scope="local"> id= </a> </span> 참조) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> metadata.version </span> </p> </td> 
   <td> <p> 문자열 </p> </td> 
   <td> <p> 메타데이터 버전 식별자. (<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0" type="reference" format="dita" scope="local"> id= </a> </span> 참조) </p> </td> 
  </tr> 
 </tbody> 
</table>

`/is/content` 요청에 대해 다음 속성이 반환됩니다.

<table id="table_B66360C475CE495D9701AB526E758873"> 
 <tbody> 
  <tr> 
   <td> <b> 속성</b> </td> 
   <td> <b> 유형</b> </td> 
   <td> <b> 설명</b> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 경로 </span> </p> </td> 
   <td> <p> 문자열 </p> </td> 
   <td> <p>파일 경로가 부분적으로 확인되었습니다. <span class="codeph"> 정적::경로 </span>을(를) 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 길이 </span> </p> </td> 
   <td> <p> int </p> </td> 
   <td> <p> 오브젝트 파일 크기(바이트) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 만료 </span> </p> </td> 
   <td> <p> 이중 </p> </td> 
   <td> <p> <span class="codeph"> 정적::Expiration </span> 또는 기본 TTL(Time to Live) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 마지막 수정일 </span> </p> </td> 
   <td> <p> 문자열 </p> </td> 
   <td> <p> 수정 날짜/시간(<span class="codeph"> 정적::TimeStamp </span> 또는 개체 파일) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> userType </span> </p> </td> 
   <td> <p> 문자열 </p> </td> 
   <td> <p> <span class="codeph"> 정적::UserType </span> </p> </td> 
  </tr> 
 </tbody> 
</table>
