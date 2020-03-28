---
description: 이미지 맵 데이터.
seo-description: 이미지 맵 데이터.
seo-title: 맵
solution: Experience Manager
title: 맵
topic: Scene7 Image Serving - Image Rendering API
uuid: 57cb0fcf-5a07-4109-bfd4-ef9aaf794b27
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 맵{#map}

이미지 맵 데이터.

`req=map[,text|{xml[, *`encoding`*]}|{json[&id= *`reqId`*]}]`

<table id="simpletable_10F2152FDF33411491FBBAFD173CA5ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 인코딩</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8| UTF-16| UTF-16LE| UTF-16BE| ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>고유 요청 식별자입니다. </p></td> 
 </tr> 
</table>

추가 명령이 지정되지 않은 단순 카탈로그 항목을 쿼리할 때 수정 없이 `catalog::Map` 반환합니다(확장되지 않음 `catalog::maxPix`).

요청에 다른 명령이 지정된 경우 이미지 데이터가 있는 것처럼 요청에 포함된 모든 `catalog::Map` 및/또는 `map=` 명령을 크기 조정, 자르기, 회전 및 레이어링함으로써 파생된 복합 이미지 맵이 `req=img`반환됩니다.

두 번째 매개 변수를 `text` 지정하거나 생략하여 응답 MIME 유형의 `HTML <AREA>` 요소 문자열 형태로 이미지 맵 데이터를 반환합니다 `text/plain`.

응답의 `xml` 형식을 HTML 대신 XML로 지정합니다. 선택적으로 텍스트 인코딩을 지정할 수 있습니다. The default is `UTF-8`.

지정된 카탈로그 개체에 대한 맵 데이터를 찾을 수 없거나 이미지를 잘라낸 후 요소가 남아 있지 않은 경우 빈 문자열(또는 빈 `<AREA>` `<AREA>` 요소)을 반환합니다.

The HTTP response is cacheable with the TTL based on `catalog::Expiration`.

JSONP 응답 형식을 지원하는 요청을 사용하면 `req=` 매개 변수의 확장 구문을 사용하여 JS 콜백 핸들러의 이름을 지정할 수 있습니다.

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 는 JSONP 응답에 있는 JS 처리기의 이름입니다. a-z, A-Z 및 0-9자만 사용할 수 있습니다. 선택 사항입니다. Default is `s7jsonResponse`.

See [Image Maps](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab).
