---
description: 요청 유효성 검사.
solution: Experience Manager
title: 유효성 확인
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 88424371-45a0-43bb-af49-2e8568b7b44c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 2%

---

# 유효성 확인{#validate}

요청 유효성 검사.

`req=validate[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_F214CDA7580A46C0B5CF14CF13AA9B0A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span> </span> </p> </td> 
  <td class="stentry"> <p>고유 요청 식별자. </p></td> 
 </tr> 
</table>

다음과 같이 요청 문자열을 구문 분석합니다 `req=img` 변수를 대체하고 참조된 개체(이미지, ICC 프로파일, 글꼴 등)를 평가하지 않고 을 지정했습니다. 구문 분석이 실패하면 표준 오류 응답이 반환되고 그렇지 않으면 다음 속성이 반환됩니다.

`request.isValid=1`

HTTP 응답을 캐시할 수 없습니다.

JSONP 응답 형식을 지원하는 요청을 사용하면 확장 구문을 사용하는 JS 콜백 핸들러의 이름을 지정할 수 있습니다. `req=` 매개 변수:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 는 JSONP 응답에 있는 JS 핸들러의 이름입니다. a-z, A-Z 및 0~9자만 허용됩니다. 선택적. 기본값은 입니다 `s7jsonResponse`.
