---
description: 이미지 카탈로그의 사용자 데이터입니다. URL 경로에 지정된 이미지 카탈로그 항목에 대한 사용자 데이터를 반환합니다.
solution: Experience Manager
title: userdata
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b1d85ea6-0e12-49a8-b1dc-4c64a672770b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 1%

---

# userdata{#userdata}

이미지 카탈로그의 사용자 데이터입니다. URL 경로에 지정된 이미지 카탈로그 항목에 대한 사용자 데이터를 반환합니다.

`req=userdata[,text|{xml[, *`인코딩`*]}|json]`

<table id="simpletable_F9D94C83865F4216BCF7987C32FACC46"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 인코딩</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
</table>

`catalog::UserData`의 컨텐츠가 반환됩니다. &#39;text&#39; 형식을 지정하면 `catalog::UserData`에 있는 `??` 의 모든 인스턴스가 줄 끝기로 대체되고 단일 선 종결자(CR/LF)가 끝에 추가됩니다. URL 경로가 유효한 카탈로그 항목으로 확인되지 않는 경우 이 응답은 단일 선 종결자로 구성됩니다. &#39;xml&#39; 또는 &#39;json&#39; 형식이 요청될 때 적절한 형식이 적용됩니다.

요청 문자열의 다른 명령은 무시됩니다.

HTTP 응답은 `catalog::Expiration`을 기준으로 TTL로 캐시할 수 있습니다.

>[!NOTE]
>
>사용자 데이터 속성 키 이름에는 콜론 문자를 사용할 수 없습니다.

JSONP 응답 형식을 지원하는 요청을 사용하면 `req=` 매개 변수의 확장 구문을 사용하여 JS 콜백 처리기의 이름을 지정할 수 있습니다.

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 는 JSONP 응답에 있는 JS 처리기의 이름입니다. a-z, A-Z 및 0-9자만 허용됩니다. 선택 사항입니다. 기본값은 `s7jsonResponse`입니다.
