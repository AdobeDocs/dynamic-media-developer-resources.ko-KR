---
description: 축소판 이미지. 카탈로그 축소판 기준을 사용하여 형식이 지정되고 크기가 조정된 이미지 데이터를 요청합니다.
solution: Experience Manager
title: tmb
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 9bdcc1c4-fe2b-4316-a472-07a533f105a0
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 0%

---

# tmb{#tmb}

축소판 이미지. 카탈로그 축소판 기준을 사용하여 형식이 지정되고 크기가 조정된 이미지 데이터를 요청합니다.

`req=tmb`

응답 데이터 형식 및 응답 MIME 유형은 `fmt=`에 의해 결정됩니다. `fit=`을 제외한 모든 명령을 지원합니다.

[축소판 크기 조정](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)을 참조하십시오.

HTTP 응답은 `catalog::Expiration` 을 기반으로 TTL로 캐시할 수 있습니다.
