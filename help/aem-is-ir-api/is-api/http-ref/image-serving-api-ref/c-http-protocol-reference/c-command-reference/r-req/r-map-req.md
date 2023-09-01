---
title: 맵
description: 이미지 맵 데이터.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3330f49a-934e-492a-804c-ace4d147c65a
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 1%

---

# 맵{#map}

이미지 맵 데이터.

`req=map[,text|{xml[, *`인코딩`*]}|{json[&id= *`reqId`*]}]`

<table id="simpletable_10F2152FDF33411491FBBAFD173CA5ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 인코딩</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>고유 요청 식별자. </p></td> 
 </tr> 
</table>

반환 `catalog::Map` 추가 명령을 지정하지 않고 단순 카탈로그 항목을 쿼리할 때 수정 없이(확장 안 함) `catalog::maxPix`).

요청에 다른 명령이 지정되어 있으면 합성 이미지 맵이 반환됩니다. 합성 이미지 맵은 모두 크기 조절, 자르기, 회전 및 레이어링하여 파생됩니다 `catalog::Map` 및/또는 `map=` 이미지 데이터가에 있는 것과 마찬가지로 요청에 포함된 명령 `req=img`.

지정 `text` 또는 두 번째 매개 변수를 생략하여 이미지 맵 데이터를 `HTML <AREA>` 응답 MIME 유형의 요소 문자열 `text/plain`.

지정 `xml` 응답 형식을 HTML 대신 XML로 지정할 수 있습니다. 텍스트 인코딩을 선택적으로 지정할 수 있습니다. 기본값은 입니다 `UTF-8`.

빈 문자열 반환(또는 비어 있음) `<AREA>` 요소) 지정된 카탈로그 개체에 대한 맵 데이터가 없거나 없는 경우 `<AREA>` 요소는 이미지를 자른 후 유지됩니다.

HTTP 응답은 다음을 기반으로 하는 TTL로 캐시할 수 있습니다. `catalog::Expiration`.

JSONP 응답 형식을 지원하는 요청을 사용하면 확장 구문을 사용하는 JS 콜백 핸들러의 이름을 지정할 수 있습니다. `req=` 매개 변수:

`req=...,json [&handler = reqHandler ]`

다음 `<reqHandler>` 는 JSONP 응답에 있는 JS 핸들러의 이름입니다. a-z, A-Z 및 0~9자만 허용됩니다. 선택적. 기본값은 입니다 `s7jsonResponse`.

다음을 참조하십시오 [이미지 맵](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab).
