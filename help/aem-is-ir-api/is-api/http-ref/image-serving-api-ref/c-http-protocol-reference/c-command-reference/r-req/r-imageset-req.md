---
description: 이미지 카탈로그의 이미지 집합 데이터입니다. URL 경로에 지정된 이미지 카탈로그 항목에 대한 이미지 세트 데이터를 반환합니다.
solution: Experience Manager
title: 이미지 집합
feature: Dynamic Media Classic,SDK/API,이미지 세트
role: Developer,Business Practitioner
exl-id: 730e7db9-47f0-4e96-8948-18b8185a5b7a
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 1%

---

# 이미지 집합{#imageset}

이미지 카탈로그의 이미지 집합 데이터입니다. URL 경로에 지정된 이미지 카탈로그 항목에 대한 이미지 세트 데이터를 반환합니다.

`req=imageset[,text|javascript|{xml[, *``*]}|{json[&id= *`encodingreqId`*]}]`

<table id="simpletable_86FF9E59B11D4C408F0D932D46CC2F8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 인코딩</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> requestId</span></span> </p></td> 
  <td class="stentry"> <p>고유한 요청 식별자입니다. </p></td> 
 </tr> 
</table>

`catalog::ImageSet`의 컨텐츠는 추가 수정 없이 반환되며(해당하는 경우 문자열 현지화 제외), 그 다음에 단일 선 종결자(CR/LF)가 옵니다. URL 경로가 유효한 카탈로그 항목으로 확인되지 않는 경우 이 응답은 단일 선 종결자로 구성됩니다.

요청 문자열의 다른 명령은 무시됩니다. HTTP 응답은 `catalog::NonImgExpiration`을 기준으로 TTL로 캐시할 수 있습니다.

JSONP 응답 형식을 지원하는 요청을 사용하면 `req=` 매개 변수의 확장 구문을 사용하여 JS 콜백 처리기의 이름을 지정할 수 있습니다.

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 는 JSONP 응답에 있는 JS 처리기의 이름입니다. a-z, A-Z 및 0-9자만 허용됩니다. 선택 사항입니다. 기본값은 `s7jsonResponse`입니다.
