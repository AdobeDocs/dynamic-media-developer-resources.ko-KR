---
description: 요청 유효성 검사.
seo-description: 요청 유효성 검사.
seo-title: 유효성 확인
solution: Experience Manager
title: 유효성 확인
topic: Scene7 Image Serving - Image Rendering API
uuid: 5322c484-2cf5-4022-9863-73fc525beb56
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 3%

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

`req=img`이(가) 지정된 것처럼 요청 문자열을 구문 분석하지만 변수를 대체하고 참조된 개체(이미지, ICC 프로필, 글꼴 등)를 평가하지 않습니다. 구문 분석이 실패하면 표준 오류 응답이 반환되고, 그렇지 않으면 다음 속성이 반환됩니다.

`request.isValid=1`

HTTP 응답을 액세스할 수 없습니다.

JSONP 응답 형식을 지원하는 요청에서는 `req=` 매개 변수의 확장 구문을 사용하여 JS 콜백 핸들러의 이름을 지정할 수 있습니다.

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 는 JSONP 응답에 있는 JS 핸들러의 이름입니다. a-z, A-Z 및 0-9자만 사용할 수 있습니다. 선택 사항입니다. 기본값은 `s7jsonResponse`입니다.
