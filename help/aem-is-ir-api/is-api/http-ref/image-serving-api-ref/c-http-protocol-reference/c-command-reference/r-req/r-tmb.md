---
description: 썸네일 이미지. 카탈로그 썸네일 기준을 사용하여 형식이 지정되고 크기가 조정된 이미지 데이터를 요청합니다.
solution: Experience Manager
title: tmb
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9bdcc1c4-fe2b-4316-a472-07a533f105a0
TQID: 'https://experienceleague.adobe.com/z4QJcR89OAXysP9RV9tZ05ipva3j0CpJYjIzL0KWCnI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 55
ht-degree: 0%

---

# tmb{#tmb}

썸네일 이미지. 카탈로그 썸네일 기준을 사용하여 형식이 지정되고 크기가 조정된 이미지 데이터를 요청합니다.

`req=tmb`

응답 데이터 형식 및 응답 MIME 형식은 `fmt=`에 의해 결정됩니다. `fit=`을(를) 제외한 모든 명령을 지원합니다.

[썸네일 크기 조정](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)을 참조하십시오.

HTTP 응답은 `catalog::Expiration`을(를) 기반으로 하는 TTL로 캐시할 수 있습니다.
