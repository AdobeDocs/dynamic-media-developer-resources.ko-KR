---
description: 디버그 요청입니다. 이 디버그 명령은 req=img와 마찬가지로 요청을 구문 분석 및 사전 처리하고, 이미지 카탈로그 조회, 카탈로그 수정자 포함, 매크로 및 변수 대체 등을 실행합니다.
solution: Experience Manager
title: 해결
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ef357c19-e725-4904-b635-102e75ff7518
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 2%

---

# 해결{#resolve}

디버그 요청입니다. 이 디버그 명령은 req=img와 마찬가지로 요청을 구문 분석 및 사전 처리하고, 이미지 카탈로그 조회, catalog::Modifier 포함, 매크로 및 변수 대체 등을 실행합니다.

`req=resolve`

최종 요청 문자열이 결과 이미지 대신 MIME 유형으로 반환됩니다 `text/plain`.

HTTP 응답을 캐시할 수 없습니다.
