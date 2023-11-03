---
description: 확대/축소는 이미지 카탈로그의 데이터를 타겟팅합니다. URL 경로에 지정된 이미지 카탈로그 항목에 대한 확대/축소 대상 데이터를 반환합니다.
solution: Experience Manager
title: 목표
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 58f7b1ad-8762-4d23-b320-6f69e75ecf63
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 1%

---

# 목표{#targets}

확대/축소는 이미지 카탈로그의 데이터를 타겟팅합니다. URL 경로에 지정된 이미지 카탈로그 항목에 대한 확대/축소 대상 데이터를 반환합니다.

`req=targets[,text|{xml[, *`인코딩`*]}|{json[&id= *`reqId`*]}]`

<table id="simpletable_D64E706258FD4A9C9C8026D97B472FCC"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 인코딩</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>고유 요청 식별자. </p></td> 
 </tr> 
</table>

의 콘텐츠 `catalog::Targets` 반환됩니다. &#39;text&#39; 형식을 요청하면 의 모든 인스턴스가 `??` 위치: `catalog::Targets` 선 터미네이터 및 한 줄 터미네이터( `CR/LF`)가 끝에 추가됩니다. URL 경로가 유효한 카탈로그 항목으로 확인되지 않으면 응답은 한 줄 종결자로만 구성됩니다. &#39;xml&#39; 또는 &#39;json&#39; 형식이 요청되면 적절한 형식이 적용됩니다.

요청 문자열의 다른 명령은 무시됩니다.

HTTP 응답은 다음을 기반으로 하는 TTL로 캐시할 수 있습니다. `catalog::Expiration`.

JSONP 응답 형식을 지원하는 요청을 사용하면 확장 구문을 사용하는 JS 콜백 핸들러의 이름을 지정할 수 있습니다. `req=` 매개 변수:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 는 JSONP 응답에 있는 JS 핸들러의 이름입니다. a-z, A-Z 및 0~9자만 허용됩니다. 선택적. 기본값은 입니다 `s7jsonResponse`.
