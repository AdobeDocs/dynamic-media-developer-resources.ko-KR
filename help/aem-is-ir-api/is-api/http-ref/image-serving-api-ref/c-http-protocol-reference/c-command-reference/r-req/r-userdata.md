---
description: 이미지 카탈로그의 사용자 데이터. URL 경로에 지정된 이미지 카탈로그 항목에 대한 사용자 데이터를 반환합니다.
seo-description: 이미지 카탈로그의 사용자 데이터. URL 경로에 지정된 이미지 카탈로그 항목에 대한 사용자 데이터를 반환합니다.
seo-title: 사용자 데이터
solution: Experience Manager
title: 사용자 데이터
topic: Scene7 Image Serving - Image Rendering API
uuid: 7a34adad-f1b6-45a7-94fe-1407845710e5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# userdata{#userdata}

이미지 카탈로그의 사용자 데이터. URL 경로에 지정된 이미지 카탈로그 항목에 대한 사용자 데이터를 반환합니다.

`req=userdata[,text|{xml[, *`인코딩`*]}|json]`

<table id="simpletable_F9D94C83865F4216BCF7987C32FACC46"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 인코딩</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8| UTF-16| UTF-16LE| UTF-16BE| ISO-8859-1</span> </p></td> 
 </tr> 
</table>

컨텐츠가 `catalog::UserData` 반환됩니다. &#39;text&#39; 형식을 지정하면 에 있는 모든 인스턴스가 줄 `??` 종결자로 `catalog::UserData`대체되며 단일 줄 종결자(CR/LF)가 끝에 추가됩니다. URL 경로가 유효한 카탈로그 항목으로 확인되지 않으면 응답은 단일 라인 종결자 하나로 구성됩니다. &#39;xml&#39; 또는 &#39;json&#39; 형식이 요청되면 적절한 서식이 적용됩니다.

요청 문자열의 다른 명령은 무시됩니다.

The HTTP response is cacheable with the TTL based on `catalog::Expiration`.

>[!NOTE]
>
>사용자 데이터 속성 키 이름에는 콜론 문자를 사용할 수 없습니다.

JSONP 응답 형식을 지원하는 요청을 사용하면 `req=` 매개 변수의 확장 구문을 사용하여 JS 콜백 핸들러의 이름을 지정할 수 있습니다.

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 는 JSONP 응답에 있는 JS 처리기의 이름입니다. a-z, A-Z 및 0-9자만 사용할 수 있습니다. 선택 사항입니다. Default is `s7jsonResponse`.
