---
description: 미디어 집합 정보.
solution: Experience Manager
title: 설정
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bc69f094-ff21-4dd7-9e10-daddb3de0c65
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 1%

---

# 설정{#set}

미디어 집합 정보.

req=set[,xml[, *`encoding`*]|{json[&amp;id=*`reqId`*]}]

<table id="simpletable_02C955F4EBAD4251A728F0FC68F432B5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 인코딩</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> reqId</span> </p></td> 
  <td class="stentry"> <p>고유 요청 식별자 </p></td> 
 </tr> 
</table>

URL 경로에 지정된 이미지 카탈로그 항목에 대해 카탈로그::ImageSet과 연결된 이미지, 비디오, 견본 및 다양한 메타데이터에 대한 정보를 반환합니다. 이 응답은 제공된 세트의 유형에 의해 결정되는 바와 같은 계층적 구조이다. &#39;xml&#39; 또는 &#39;json&#39; 형식이 요청되면 적절한 형식이 적용됩니다.

`catalog::NonImgExpiration`을(를) 기반으로 하는 TTL로 HTTP 응답을 캐시할 수 있습니다.

>[!NOTE]
>
>콜론 문자는 req=set 요청에서 허용되지 않습니다.

JSON 응답 형식을 지원하는 요청을 사용하면 `req=` 매개 변수의 확장 구문을 사용하여 JS 콜백 처리기의 이름을 지정할 수 있습니다.

`req=...,json [&handler = reqHandler ]`

`<reqHandler>`은(는) JSONP 응답에 있는 JS 처리기의 이름입니다. a-z, A-Z 및 0~9자만 허용됩니다. 선택 사항입니다. 기본값은 `s7jsonResponse`입니다.
