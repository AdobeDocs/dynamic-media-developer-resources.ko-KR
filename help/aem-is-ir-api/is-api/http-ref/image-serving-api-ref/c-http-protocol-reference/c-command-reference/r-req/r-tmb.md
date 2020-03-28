---
description: 축소판 이미지. 카탈로그 축소판 기준을 사용하여 이미지 데이터의 형식 및 크기를 요청합니다.
seo-description: 축소판 이미지. 카탈로그 축소판 기준을 사용하여 이미지 데이터의 형식 및 크기를 요청합니다.
seo-title: tmb
solution: Experience Manager
title: tmb
topic: Scene7 Image Serving - Image Rendering API
uuid: 0f098c30-a164-47a6-abb2-0eb1d0bc24da
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# tmb{#tmb}

축소판 이미지. 카탈로그 축소판 기준을 사용하여 이미지 데이터의 형식 및 크기를 요청합니다.

`req=tmb`

응답 데이터 형식 및 응답 MIME 형식은 에 의해 결정됩니다 `fmt=`. 를 제외한 모든 명령을 `fit=`지원합니다.

축소판 [크기 조정을 참조하십시오](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f).

HTTP 응답은 TTL을 기준으로 캐시될 수 `catalog::Expiration`있습니다.
