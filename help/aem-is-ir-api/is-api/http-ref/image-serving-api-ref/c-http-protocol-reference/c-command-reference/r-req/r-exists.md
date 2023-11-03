---
description: 이미지가 존재합니다.
solution: Experience Manager
title: 존재
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 810453f0-7b35-4eed-8b23-6b59a8300c50
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 2%

---

# 존재{#exists}

이미지가 존재합니다.

`req=exists[,text|javascript|xml|{json[&id= *`reqId`*]}]`

*`reqId`* 고유 요청 식별자

다음 이름의 단일 속성을 반환합니다. `catalogRecord.exists`. 지정된 카탈로그 항목이 이미지 또는 기본 카탈로그에 있는 경우 속성 값은 &quot;1&quot;로 설정되고, 그렇지 않은 경우 속성 값은 &quot;0&quot;으로 설정됩니다. `req=exists` 에 대한 요청 `/is/content` 컨텍스트는 정적 콘텐츠 카탈로그에 지정된 레코드의 존재 여부를 나타냅니다.

요청 문자열의 다른 명령은 무시됩니다. HTTP 응답은 다음을 기반으로 하는 TTL로 캐시할 수 있습니다. `attribute::NonImgExpiration`.

JSONP 응답 형식을 지원하는 요청을 사용하면 확장 구문을 사용하는 JS 콜백 핸들러의 이름을 지정할 수 있습니다. `req=` 매개 변수:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 는 JSONP 응답에 있는 JS 핸들러의 이름입니다. a-z, A-Z 및 0~9자만 허용됩니다. 선택적. 기본값은 입니다 `s7jsonResponse`.
