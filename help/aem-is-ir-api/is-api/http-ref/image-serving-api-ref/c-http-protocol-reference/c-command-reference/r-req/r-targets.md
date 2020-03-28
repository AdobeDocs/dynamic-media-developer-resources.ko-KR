---
description: 이미지 카탈로그에서 대상 데이터를 확대/축소합니다. URL 경로에 지정된 이미지 카탈로그 항목의 확대/축소 대상 데이터를 반환합니다.
seo-description: 이미지 카탈로그에서 대상 데이터를 확대/축소합니다. URL 경로에 지정된 이미지 카탈로그 항목의 확대/축소 대상 데이터를 반환합니다.
seo-title: 목표
solution: Experience Manager
title: 목표
topic: Scene7 Image Serving - Image Rendering API
uuid: e20dcd2c-913a-4153-97c7-dfb190763e39
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 목표{#targets}

이미지 카탈로그에서 대상 데이터를 확대/축소합니다. URL 경로에 지정된 이미지 카탈로그 항목의 확대/축소 대상 데이터를 반환합니다.

`req=targets[,text|{xml[, *`encoding`*]}|{json[&id= *`reqId`*]}]`

<table id="simpletable_D64E706258FD4A9C9C8026D97B472FCC"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 인코딩</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8| UTF-16| UTF-16LE| UTF-16BE| ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>고유 요청 식별자입니다. </p></td> 
 </tr> 
</table>

컨텐츠가 `catalog::Targets` 반환됩니다. &#39;text&#39; 형식이 요청되면 `??` 에 있는 모든 인스턴스가 `catalog::Targets` 줄 종결자로 대체되고 단일 줄 종결자( `CR/LF`)가 끝에 추가됩니다. URL 경로가 유효한 카탈로그 항목으로 확인되지 않으면 응답은 단일 라인 종결자 하나로 구성됩니다. &#39;xml&#39; 또는 &#39;json&#39; 형식이 요청되면 적절한 서식이 적용됩니다.

요청 문자열의 다른 명령은 무시됩니다.

The HTTP response is cacheable with the TTL based on `catalog::Expiration`.

JSONP 응답 형식을 지원하는 요청을 사용하면 `req=` 매개 변수의 확장 구문을 사용하여 JS 콜백 핸들러의 이름을 지정할 수 있습니다.

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 는 JSONP 응답에 있는 JS 처리기의 이름입니다. a-z, A-Z 및 0-9자만 사용할 수 있습니다. 선택 사항입니다. Default is `s7jsonResponse`.
