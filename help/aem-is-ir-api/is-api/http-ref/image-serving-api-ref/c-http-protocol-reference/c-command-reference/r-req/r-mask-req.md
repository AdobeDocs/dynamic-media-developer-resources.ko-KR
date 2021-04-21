---
description: 이미지 마스크. 마스크(알파 채널) 데이터를 요청합니다.
solution: Experience Manager
title: 마스크
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: ddfccb4ca157764e39fc719d96b63e6ee95304bf
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 0%

---


# mask{#mask}

이미지 마스크. 마스크(알파 채널) 데이터를 요청합니다.

`req=mask`

`req=img`과 동일한 명령을 지원합니다. 서버에서 동일한 방식으로 처리되지만 RGB 또는 RGBA 데이터를 반환하는 대신 색상 정보를 삭제하고 마스크(알파 채널) 데이터만 반환합니다. 응답 데이터 형식 및 응답 MIME 유형은 `fmt=`으로 결정됩니다.

HTTP 응답은 `catalog::Expiration`을(를) 기준으로 TTL을 사용하여 액세스할 수 있습니다.
