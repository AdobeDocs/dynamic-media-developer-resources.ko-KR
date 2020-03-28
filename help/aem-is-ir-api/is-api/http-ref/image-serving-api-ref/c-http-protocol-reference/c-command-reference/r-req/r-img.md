---
description: 이미지(기본값). 표준 이미지 데이터를 요청합니다.
seo-description: 이미지(기본값). 표준 이미지 데이터를 요청합니다.
seo-title: img
solution: Experience Manager
title: img
topic: Scene7 Image Serving - Image Rendering API
uuid: 4809f916-0ccf-4a24-a93b-c51ed6203061
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# img{#img}

이미지(기본값). 표준 이미지 데이터를 요청합니다.

`req=img`

응답 데이터 형식 및 응답 MIME 형식은 에 의해 결정됩니다 `fmt=`. `req=img` 는 기본 요청 유형이며 명시적으로 지정할 필요가 없습니다. The HTTP response is cacheable with the TTL based on `catalog::Expiration`.

다른 요청 명령은 문서화된 대로 적용됩니다.
