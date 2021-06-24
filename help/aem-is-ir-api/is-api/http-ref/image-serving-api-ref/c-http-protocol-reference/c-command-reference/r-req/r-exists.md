---
description: 이미지가 있습니다.
solution: Experience Manager
title: 존재
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 810453f0-7b35-4eed-8b23-6b59a8300c50
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 2%

---

# 존재{#exists}

이미지가 있습니다.

`req=exists[,text|javascript|xml|{json[&id= *`reqId`*]}]`

*`reqId`* 고유 요청 식별자

`catalogRecord.exists`이라는 단일 속성을 반환합니다. 지정된 카탈로그 항목이 이미지 또는 기본 카탈로그에 있으면 속성 값이 &quot;1&quot;로 설정되어 있고 그렇지 않으면 &quot;0&quot;으로 설정됩니다. `req=exists` 컨텍스트에  `/is/content` 대한 요청은 정적 컨텐츠 카탈로그에 지정된 레코드가 있는지 여부를 나타냅니다.

요청 문자열의 다른 명령은 무시됩니다. HTTP 응답은 `attribute::NonImgExpiration`을 기준으로 TTL로 캐시할 수 있습니다.

JSONP 응답 형식을 지원하는 요청을 사용하면 `req=` 매개 변수의 확장 구문을 사용하여 JS 콜백 처리기의 이름을 지정할 수 있습니다.

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 는 JSONP 응답에 있는 JS 처리기의 이름입니다. a-z, A-Z 및 0-9자만 허용됩니다. 선택 사항입니다. 기본값은 `s7jsonResponse`입니다.
