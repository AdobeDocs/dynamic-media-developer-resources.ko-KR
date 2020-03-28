---
description: 사용 가능한 로케일별 버전. 요청 경로에 지정된 카탈로그 ID의 사용 가능한 로케일별 버전 목록을 반환합니다.
seo-description: 사용 가능한 로케일별 버전. 요청 경로에 지정된 카탈로그 ID의 사용 가능한 로케일별 버전 목록을 반환합니다.
seo-title: xlate
solution: Experience Manager
title: xlate
topic: Scene7 Image Serving - Image Rendering API
uuid: 4c2370e5-1d46-4242-89bb-a5ce416ef63c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# xlate{#xlate}

사용 가능한 로케일별 버전. 요청 경로에 지정된 카탈로그 ID의 사용 가능한 로케일별 버전 목록을 반환합니다.

`req=xlate[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_8970A3A5A64F4DC2B184E251993390C5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>고유 요청 식별자입니다. </p></td> 
 </tr> 
</table>

개체 [ID 변환을 참조하십시오](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md#reference-cf3e34e6cbb346d69ded9982bfdef414).

예:

`xlate.translatedIds=image,image_fr,image_de`

The HTTP response is cacheable with the TTL based on `catalog::Expiration`.

JSONP 응답 형식을 지원하는 요청을 사용하면 `req=` 매개 변수의 확장 구문을 사용하여 JS 콜백 핸들러의 이름을 지정할 수 있습니다.

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 는 JSONP 응답에 있는 JS 처리기의 이름입니다. a-z, A-Z 및 0-9자만 사용할 수 있습니다. 선택 사항입니다. Default is `s7jsonResponse`.
