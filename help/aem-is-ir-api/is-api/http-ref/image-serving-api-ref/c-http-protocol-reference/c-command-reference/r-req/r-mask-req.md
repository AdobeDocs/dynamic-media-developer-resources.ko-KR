---
description: 이미지 마스크. 마스크(알파 채널) 데이터를 요청합니다.
seo-description: 이미지 마스크. 마스크(알파 채널) 데이터를 요청합니다.
seo-title: 마스크
solution: Experience Manager
title: 마스크
topic: Scene7 Image Serving - Image Rendering API
uuid: 9a8dc4bc-0757-45d2-adfe-d4bd69b4efa9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# mask{#mask}

이미지 마스크. 마스크(알파 채널) 데이터를 요청합니다.

`req=mask`

서버와 동일한 명령을 `req=img`지원하며 서버에서 동일한 방식으로 처리되지만 RGB 또는 RGBA 데이터를 반환하는 대신 색상 정보를 삭제하고 마스크(알파 채널) 데이터만 반환합니다. 응답 데이터 형식 및 응답 MIME 형식은 에 의해 결정됩니다 `fmt=`.

The HTTP response is cacheable with the TTL based on `catalog::Expiration`.
