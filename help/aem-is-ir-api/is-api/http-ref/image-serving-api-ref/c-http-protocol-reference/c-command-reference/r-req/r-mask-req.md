---
description: 이미지 마스크입니다. 마스크(알파 채널) 데이터를 요청합니다.
solution: Experience Manager
title: 마스크
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0e743fe5-a623-4f5f-bc61-536ed70532bf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 0%

---

# 마스크{#mask}

이미지 마스크입니다. 마스크(알파 채널) 데이터를 요청합니다.

`req=mask`

와 동일한 명령 지원 `req=img`. 서버에서 동일한 방식으로 처리되지만 RGB 또는 RGBA 데이터를 반환하는 대신 색상 정보가 삭제되고 마스크(알파 채널) 데이터만 반환됩니다. 응답 데이터 형식 및 응답 MIME 유형은 다음을 통해 결정됩니다. `fmt=`.

HTTP 응답은 다음을 기반으로 하는 TTL로 캐시할 수 있습니다. `catalog::Expiration`.
