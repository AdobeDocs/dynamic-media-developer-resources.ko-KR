---
description: 이미지가 존재합니다.
solution: Experience Manager
title: 존재
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 810453f0-7b35-4eed-8b23-6b59a8300c50
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 1%

---

# 존재{#exists}

이미지가 존재합니다.

`req=exists[,text|javascript|xml|{json[&id= *`reqId`*]}]`

*`reqId`* 고유 요청 식별자

이름이 `catalogRecord.exists`인 단일 속성을 반환합니다. 지정된 카탈로그 항목이 이미지 또는 기본 카탈로그에 있는 경우 속성 값은 &quot;1&quot;로 설정되고, 그렇지 않은 경우 속성 값은 &quot;0&quot;으로 설정됩니다. `/is/content` 컨텍스트에 대한 `req=exists` 요청은 정적 콘텐츠 카탈로그에 지정된 레코드가 있는지 여부를 나타냅니다.

요청 문자열의 다른 명령은 무시됩니다. `attribute::NonImgExpiration`을(를) 기반으로 하는 TTL로 HTTP 응답을 캐시할 수 있습니다.

JSONP 응답 형식을 지원하는 요청을 사용하면 `req=` 매개 변수의 확장 구문을 사용하여 JS 콜백 처리기의 이름을 지정할 수 있습니다.

`req=...,json [&handler = reqHandler ]`

`<reqHandler>`은(는) JSONP 응답에 있는 JS 처리기의 이름입니다. a-z, A-Z 및 0~9자만 허용됩니다. 선택 사항입니다. 기본값은 `s7jsonResponse`입니다.
