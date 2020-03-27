---
description: 기본 클라이언트 캐시 시간을 라이브로 설정합니다. 특정 카탈로그 레코드에 유효한 카탈로그 만료 값이 없는 경우 기본 만료 간격을 제공합니다.
seo-description: 기본 클라이언트 캐시 시간을 라이브로 설정합니다. 특정 카탈로그 레코드에 유효한 카탈로그 만료 값이 없는 경우 기본 만료 간격을 제공합니다.
seo-title: 만료
solution: Experience Manager
title: 만료
topic: Scene7 Image Serving - Image Rendering API
uuid: 26b2abee-8bd1-4011-90ff-f5143826ac0d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 만료{#expiration}

기본 클라이언트 캐시 시간을 라이브로 설정합니다. 특정 카탈로그 레코드에 유효한 카탈로그:Expiration 값이 포함되어 있지 않은 경우 기본 만료 간격을 제공합니다.

## 속성 {#section-063be3b2f13a48a3a5ab8080718e9812}

실수, 0 이상 회신 데이터가 생성된 이후 만료까지 남은 시간. 응답 이미지를 항상 즉시 만료되도록 0으로 설정하면 클라이언트 캐싱을 효과적으로 사용할 수 없게 됩니다. -1로 `never expire`설정하면

## 기본값 {#section-f55308b195c04083996f6717c8537634}

정의되지 않았거나 비어 있는 `default::Expiration` 경우 상속됩니다.

TTL(Time-To-Live)은 캐시가 만료되기 전의 기간입니다. 기본 TTL 파섹

## 참조 {#section-b2411d99ddb14115ad475d506efd8967}

[catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [attribute::DefaultExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf), [속성::NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
