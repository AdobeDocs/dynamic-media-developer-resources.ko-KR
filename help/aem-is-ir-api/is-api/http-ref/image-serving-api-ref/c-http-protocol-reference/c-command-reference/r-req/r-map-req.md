---
description: 이미지 맵 데이터.
seo-description: 이미지 맵 데이터.
seo-title: 맵
solution: Experience Manager
title: 맵
uuid: 57cb0fcf-5a07-4109-bfd4-ef9aaf794b27
feature: Dynamic Media Classic,SDK/API
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 2%

---


# 맵{#map}

이미지 맵 데이터.

`req=map[,text|{xml[, *`encoding `*]}|{json[&id= *`reqId`*]}]`

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

추가 명령이 지정되지 않은 단순 카탈로그 항목을 쿼리할 때 수정 없이 `catalog::Map`을 반환합니다(는 `catalog::maxPix`까지 크기 조절되지 않음).

요청에 다른 명령이 지정된 경우 이미지 데이터가 `req=img`에 있는 것처럼 요청에 포함된 모든 `catalog::Map` 및/또는 `map=` 명령을 크기 조절, 자르기, 회전 및 레이어로 파생되는 합성 이미지 맵이 반환됩니다.

`text`을 지정하거나 두 번째 매개 변수를 생략하여 응답 MIME 유형이 `text/plain`인 `HTML <AREA>` 요소 문자열 형태로 이미지 맵 데이터를 반환합니다.

응답의 형식을 HTML 대신 XML로 지정하려면 `xml`을 지정합니다. 텍스트 인코딩은 선택적으로 지정할 수 있습니다. 기본값은 `UTF-8`입니다.

지정된 카탈로그 개체에 대한 맵 데이터를 찾을 수 없거나 이미지를 잘라낸 후 `<AREA>` 요소가 남아 있지 않으면 빈 문자열(또는 `<AREA>` 요소)을 반환합니다.

HTTP 응답은 `catalog::Expiration`을(를) 기준으로 TTL을 사용하여 액세스할 수 있습니다.

JSONP 응답 형식을 지원하는 요청에서는 `req=` 매개 변수의 확장 구문을 사용하여 JS 콜백 핸들러의 이름을 지정할 수 있습니다.

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 는 JSONP 응답에 있는 JS 핸들러의 이름입니다. a-z, A-Z 및 0-9자만 사용할 수 있습니다. 선택 사항입니다. 기본값은 `s7jsonResponse`입니다.

[이미지 맵](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab)을(를) 참조하십시오.
