---
description: 이미지 마스크입니다. 마스크(알파 채널) 데이터를 요청합니다.
solution: Experience Manager
title: 마스크
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0e743fe5-a623-4f5f-bc61-536ed70532bf
TQID: 'https://experienceleague.adobe.com/FMsQMZsc3N1ToEzXBE0vOzkezfemSzT6NaGJQ1gQqd8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 76
ht-degree: 0%

---

# 마스크{#mask}

이미지 마스크입니다. 마스크(알파 채널) 데이터를 요청합니다.

`req=mask`

`req=img`과(와) 동일한 명령을 지원합니다. 서버에서 동일한 방식으로 처리되지만 RGB 또는 RGBA 데이터를 반환하는 대신 색상 정보가 삭제되고 마스크(알파 채널) 데이터만 반환됩니다. 응답 데이터 형식 및 응답 MIME 형식은 `fmt=`에 의해 결정됩니다.

`catalog::Expiration`을(를) 기반으로 하는 TTL로 HTTP 응답을 캐시할 수 있습니다.
