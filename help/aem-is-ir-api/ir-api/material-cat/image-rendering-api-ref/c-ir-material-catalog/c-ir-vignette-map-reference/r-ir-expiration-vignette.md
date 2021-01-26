---
description: 클라이언트의 실시간 캐시 시간 만료까지 남은 시간. 클라이언트 및 프록시 서버 캐싱을 관리하는 데 사용됩니다.
seo-description: 클라이언트의 실시간 캐시 시간 만료까지 남은 시간. 클라이언트 및 프록시 서버 캐싱을 관리하는 데 사용됩니다.
seo-title: 만료
solution: Experience Manager
title: 만료
topic: Dynamic Media Image Serving - Image Rendering API
uuid: fa267728-9a36-4705-97d6-d567148fc2d7
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 6%

---


# 만료{#expiration}

클라이언트의 실시간 캐시 시간 만료까지 남은 시간. 클라이언트 및 프록시 서버 캐싱을 관리하는 데 사용됩니다.

자세한 내용은 ` [catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce)`를 참조하십시오.

## 속성 {#section-dcdd44cc3f0a4849b968dbd4f1e3768a}

실수, -2, -1, 0 이상. 응답 이미지가 생성된 이후 만료까지 남은 시간. 응답 이미지를 항상 즉시 만료되도록 0으로 설정하면 클라이언트 캐싱을 효과적으로 사용할 수 없습니다. `never expire`;으로 표시하려면 -1로 설정합니다.이 경우 서버는 파일이 실제로 변경되었는지 여부를 확인하지 않고 조건부 `GET` 요청에 응답하여 항상 403 상태를 반환합니다. `attribute::Expiration`에서 제공하는 기본값을 사용하려면 -2로 설정합니다.

## 기본값 {#section-fb8ea80975034b49af7510764758f123}

`attribute::Expiration` 값이 -2인 경우, 또는 필드가 비어 있는 경우에 사용됩니다.

## 참조 {#section-a0d3dab0f6db49b58f1f935d3bdea2fd}

[속성::만료](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996) ,  [카탈로그::만료](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce),  [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
