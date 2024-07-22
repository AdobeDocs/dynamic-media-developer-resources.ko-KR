---
title: 맵
description: 이미지 맵 데이터.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3330f49a-934e-492a-804c-ace4d147c65a
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 0%

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

추가 명령이 지정되지 않은(`catalog::maxPix`(으)로 확장되지 않음) 단순 카탈로그 항목을 쿼리할 때 수정하지 않고 `catalog::Map`을(를) 반환합니다.

요청에 다른 명령이 지정되어 있으면 합성 이미지 맵이 반환됩니다. 복합 이미지 맵은 이미지 데이터가 `req=img`에 있는 것처럼 요청에 포함된 모든 `catalog::Map` 및/또는 `map=` 명령의 크기 조절, 자르기, 회전 및 계층화를 통해 파생됩니다.

응답 MIME 형식이 `text/plain`인 `HTML <AREA>` 요소 문자열 형식으로 이미지 맵 데이터를 반환할 수 있도록 `text`을(를) 지정하거나 두 번째 매개 변수를 생략합니다.

응답을 HTML 대신 XML로 포맷할 수 있도록 `xml`을(를) 지정하십시오. 텍스트 인코딩을 선택적으로 지정할 수 있습니다. 기본값은 `UTF-8`입니다.

지정된 카탈로그 개체에 대한 맵 데이터가 없거나 이미지를 자른 후 `<AREA>` 요소가 남아 있지 않으면 빈 문자열(또는 빈 `<AREA>` 요소)을 반환합니다.

`catalog::Expiration`을(를) 기반으로 하는 TTL로 HTTP 응답을 캐시할 수 있습니다.

JSONP 응답 형식을 지원하는 요청을 사용하면 `req=` 매개 변수의 확장 구문을 사용하여 JS 콜백 처리기의 이름을 지정할 수 있습니다.

`req=...,json [&handler = reqHandler ]`

`<reqHandler>`은(는) JSONP 응답에 있는 JS 처리기의 이름입니다. a-z, A-Z 및 0~9자만 허용됩니다. 선택 사항입니다. 기본값은 `s7jsonResponse`입니다.

[이미지 맵](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab)을 참조하세요.
