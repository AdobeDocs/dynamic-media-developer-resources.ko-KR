---
description: 클라이언트 캐시 사용 시간 만료까지 남은 시간 수입니다. 클라이언트 및 프록시 서버 캐싱을 관리하는 데 사용됩니다.
solution: Experience Manager
title: 만료
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5717d568-467e-495b-b963-9b3d42e866a6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 6%

---

# 만료{#expiration}

클라이언트 캐시 사용 시간 만료까지 남은 시간 수입니다. 클라이언트 및 프록시 서버 캐싱을 관리하는 데 사용됩니다.

자세한 내용은 ` [catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce)`를 참조하십시오.

## 속성 {#section-dcdd44cc3f0a4849b968dbd4f1e3768a}

실수, -2, -1, 0 이상 응답 이미지가 생성된 이후 만료까지 남은 시간. 항상 응답 이미지를 즉시 만료하도록 0으로 설정하면 클라이언트 캐싱을 효과적으로 사용하지 않습니다. `never expire`;(으)로 표시하려면 -1로 설정합니다. 이 경우 파일이 실제로 변경되었는지 여부를 확인하지 않고 서버는 조건부 `GET` 요청에 응답하여 항상 403 상태를 반환합니다. `attribute::Expiration`에서 제공한 기본값을 사용하려면 -2로 설정하십시오.

## 기본값 {#section-fb8ea80975034b49af7510764758f123}

`attribute::Expiration` 필드가 없거나, 값이 -2이거나, 필드가 비어 있는 경우 사용됩니다.

## 참조 {#section-a0d3dab0f6db49b58f1f935d3bdea2fd}

[속성::만료](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996) ,  [카탈로그::만료](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce),  [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
