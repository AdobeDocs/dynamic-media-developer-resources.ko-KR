---
title: img
description: 이미지(기본값). 표준 이미지 데이터를 요청합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5338358e-755b-41d6-a941-8754d0deb9aa
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 0%

---

# img{#img}

이미지(기본값). 표준 이미지 데이터를 요청합니다.

`req=img`

응답 데이터 형식 및 응답 MIME 유형은 다음을 통해 결정됩니다. `fmt=`. 수정자 `req=img` 는 기본 요청 유형이며 명시적으로 필요하지 않습니다. HTTP 응답은 다음을 기반으로 하는 TTL로 캐시할 수 있습니다. `catalog::Expiration`.

다른 요청 명령은 문서화된 대로 적용됩니다.
