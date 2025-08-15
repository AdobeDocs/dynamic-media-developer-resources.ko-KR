---
description: 확대/축소는 이미지 카탈로그의 데이터를 타겟팅합니다. URL 경로에 지정된 이미지 카탈로그 항목에 대한 확대/축소 대상 데이터를 반환합니다.
solution: Experience Manager
title: 목표
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 58f7b1ad-8762-4d23-b320-6f69e75ecf63
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '185'
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

`catalog::Targets`의 콘텐츠가 반환됩니다. &#39;text&#39; 형식이 요청되면 `??`에서 `catalog::Targets`의 모든 인스턴스가 줄 종결자로 대체되고 한 줄 종결자(`CR/LF`)가 끝에 추가됩니다. URL 경로가 유효한 카탈로그 항목으로 확인되지 않으면 응답은 한 줄 종결자로만 구성됩니다. &#39;xml&#39; 또는 &#39;json&#39; 형식이 요청되면 적절한 형식이 적용됩니다.

요청 문자열의 다른 명령은 무시됩니다.

`catalog::Expiration`을(를) 기반으로 하는 TTL로 HTTP 응답을 캐시할 수 있습니다.

JSONP 응답 형식을 지원하는 요청을 사용하면 `req=` 매개 변수의 확장 구문을 사용하여 JS 콜백 처리기의 이름을 지정할 수 있습니다.

`req=...,json [&handler = reqHandler ]`

`<reqHandler>`은(는) JSONP 응답에 있는 JS 처리기의 이름입니다. a-z, A-Z 및 0~9자만 허용됩니다. 선택 사항입니다. 기본값은 `s7jsonResponse`입니다.
