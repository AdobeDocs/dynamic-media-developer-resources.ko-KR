---
title: 해결
description: 디버그 요청입니다. 이 디버그 명령은 req=img와 마찬가지로 요청을 구문 분석 및 사전 처리하고, 이미지 카탈로그 조회, 카탈로그 수정자 포함, 매크로 및 변수 대체 등을 실행합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ef357c19-e725-4904-b635-102e75ff7518
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 2%

---

# 해결{#resolve}

디버그 요청입니다. 이 디버그 명령은 req=img와 마찬가지로 요청을 구문 분석 및 사전 처리하고, 이미지 카탈로그 조회, catalog::Modifier 포함, 매크로 및 변수 대체 등을 실행합니다.

`req=resolve`

MIME 유형이 `text/plain`인 결과 이미지 대신 최종 요청 문자열이 반환됩니다.

HTTP 응답을 캐시할 수 없습니다.
