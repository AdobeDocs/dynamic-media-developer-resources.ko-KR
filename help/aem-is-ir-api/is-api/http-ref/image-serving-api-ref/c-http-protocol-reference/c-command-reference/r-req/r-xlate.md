---
description: 사용 가능한 로케일 특정 버전. 요청 경로에 지정된 카탈로그 ID의 사용 가능한 로케일 특정 버전 목록을 반환합니다.
solution: Experience Manager
title: xlate
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: bf5b3cb7-9792-4eca-a1aa-55aa4089b4d4
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 2%

---

# xlate{#xlate}

사용 가능한 로케일 특정 버전. 요청 경로에 지정된 카탈로그 ID의 사용 가능한 로케일 특정 버전 목록을 반환합니다.

`req=xlate[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_8970A3A5A64F4DC2B184E251993390C5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>고유한 요청 식별자입니다. </p></td> 
 </tr> 
</table>

[개체 Id 변환](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md#reference-cf3e34e6cbb346d69ded9982bfdef414)을 참조하십시오.

예:

`xlate.translatedIds=image,image_fr,image_de`

HTTP 응답은 `catalog::Expiration`을 기준으로 TTL로 캐시할 수 있습니다.

JSONP 응답 형식을 지원하는 요청을 사용하면 `req=` 매개 변수의 확장 구문을 사용하여 JS 콜백 처리기의 이름을 지정할 수 있습니다.

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 는 JSONP 응답에 있는 JS 처리기의 이름입니다. a-z, A-Z 및 0-9자만 허용됩니다. 선택 사항입니다. 기본값은 `s7jsonResponse`입니다.
