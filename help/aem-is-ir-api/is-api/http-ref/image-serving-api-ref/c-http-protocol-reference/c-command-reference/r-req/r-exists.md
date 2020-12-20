---
description: 이미지가 있습니다.
seo-description: 이미지가 있습니다.
seo-title: 존재
solution: Experience Manager
title: 존재
topic: Scene7 Image Serving - Image Rendering API
uuid: 5490e4c7-b52a-4b2e-b002-34afaa242c08
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---


# 존재{#exists}

이미지가 있습니다.

`req=exists[,text|javascript|xml|{json[&id= *`reqId`*]}]`

*`reqId`* 고유 요청 식별자

`catalogRecord.exists`이라는 단일 속성을 반환합니다. 이미지 또는 기본 카탈로그에 지정된 카탈로그 항목이 있는 경우 속성 값은 &quot;1&quot;로 설정되며, 그렇지 않은 경우 &quot;0&quot;으로 설정됩니다. `req=exists` 컨텍스트에 대한  `/is/content` 요청은 정적 컨텐츠 카탈로그에 지정된 레코드가 있는지 여부를 나타냅니다.

요청 문자열의 다른 명령은 무시됩니다. HTTP 응답은 `attribute::NonImgExpiration`을(를) 기준으로 TTL을 사용하여 액세스할 수 있습니다.

JSONP 응답 형식을 지원하는 요청에서는 `req=` 매개 변수의 확장 구문을 사용하여 JS 콜백 핸들러의 이름을 지정할 수 있습니다.

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 는 JSONP 응답에 있는 JS 핸들러의 이름입니다. a-z, A-Z 및 0-9자만 사용할 수 있습니다. 선택 사항입니다. 기본값은 `s7jsonResponse`입니다.
