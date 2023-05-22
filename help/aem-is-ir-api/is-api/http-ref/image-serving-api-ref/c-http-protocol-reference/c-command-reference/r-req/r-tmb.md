---
description: 썸네일 이미지. 카탈로그 썸네일 기준을 사용하여 형식이 지정되고 크기가 조정된 이미지 데이터를 요청합니다.
solution: Experience Manager
title: tmb
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9bdcc1c4-fe2b-4316-a472-07a533f105a0
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 0%

---

# tmb{#tmb}

썸네일 이미지. 카탈로그 썸네일 기준을 사용하여 형식이 지정되고 크기가 조정된 이미지 데이터를 요청합니다.

`req=tmb`

응답 데이터 형식 및 응답 MIME 유형은 다음을 통해 결정됩니다. `fmt=`. 다음을 제외한 모든 명령 지원 `fit=`.

다음을 참조하십시오 [썸네일 크기 조정](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f).

HTTP 응답은 다음을 기반으로 하는 TTL로 캐시할 수 있습니다. `catalog::Expiration`.
