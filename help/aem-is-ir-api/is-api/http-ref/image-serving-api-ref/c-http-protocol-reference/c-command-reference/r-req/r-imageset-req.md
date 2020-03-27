---
description: 이미지 카탈로그의 이미지 집합 데이터. URL 경로에 지정된 이미지 카탈로그 항목에 대한 이미지 집합 데이터를 반환합니다.
seo-description: 이미지 카탈로그의 이미지 집합 데이터. URL 경로에 지정된 이미지 카탈로그 항목에 대한 이미지 집합 데이터를 반환합니다.
seo-title: 이미지 집합
solution: Experience Manager
title: 이미지 집합
topic: Scene7 Image Serving - Image Rendering API
uuid: 8854e903-a85f-403a-ae3d-b7281a236262
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# imageset{#imageset}

이미지 카탈로그의 이미지 집합 데이터. URL 경로에 지정된 이미지 카탈로그 항목에 대한 이미지 집합 데이터를 반환합니다.

`req=imageset[,text|javascript|{xml[, *`encoding`*]}|{json[&id= *`reqId`*]}]`

<table id="simpletable_86FF9E59B11D4C408F0D932D46CC2F8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 인코딩</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8| UTF-16| UTF-16LE| UTF-16BE| ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> requestId</span></span> </p></td> 
  <td class="stentry"> <p>고유 요청 식별자입니다. </p></td> 
 </tr> 
</table>

의 컨텐츠는 추가 수정 없이 `catalog::ImageSet` 반환되며(해당되는 경우 문자열 현지화 제외), 한 줄 종결자(CR/LF)가 반환됩니다. URL 경로가 유효한 카탈로그 항목으로 확인되지 않으면 응답은 단일 라인 종결자 하나로 구성됩니다.

요청 문자열의 다른 명령은 무시됩니다. The HTTP response is cacheable with the TTL based on `catalog::NonImgExpiration`.

JSONP 응답 형식을 지원하는 요청을 사용하면 `req=` 매개 변수의 확장 구문을 사용하여 JS 콜백 핸들러의 이름을 지정할 수 있습니다.

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 는 JSONP 응답에 있는 JS 처리기의 이름입니다. a-z, A-Z 및 0-9자만 사용할 수 있습니다. 선택 사항입니다. Default is `s7jsonResponse`.
