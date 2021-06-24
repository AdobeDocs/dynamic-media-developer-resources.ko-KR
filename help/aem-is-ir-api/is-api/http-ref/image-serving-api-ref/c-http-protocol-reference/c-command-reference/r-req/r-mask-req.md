---
description: 이미지 마스크. 마스크(알파 채널) 데이터를 요청합니다.
solution: Experience Manager
title: 마스크
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 0e743fe5-a623-4f5f-bc61-536ed70532bf
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 0%

---

# 마스크{#mask}

이미지 마스크. 마스크(알파 채널) 데이터를 요청합니다.

`req=mask`

`req=img`과 동일한 명령을 지원합니다. 서버에서 동일한 방식으로 처리되지만 RGB 또는 RGBA 데이터를 반환하는 대신 색상 정보를 무시하고 마스크(알파 채널) 데이터만 반환합니다. 응답 데이터 형식 및 응답 MIME 유형은 `fmt=`에 의해 결정됩니다.

HTTP 응답은 `catalog::Expiration`을 기준으로 TTL로 캐시할 수 있습니다.
