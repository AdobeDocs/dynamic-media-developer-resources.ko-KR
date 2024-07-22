---
description: 기본 클라이언트 캐시 TTL(Time to Live). 특정 카탈로그 레코드에 유효한 카탈로그 만료 값이 없는 경우 기본 만료 간격을 제공합니다.
solution: Experience Manager
title: 만료
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c9dccf8d-56b3-4608-ac05-9c17babc609e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 4%

---

# 만료{#expiration}

기본 클라이언트 캐시 TTL(Time to Live). 특정 카탈로그 레코드에 유효한 카탈로그::Expiration 값이 없는 경우 기본 만료 간격을 제공합니다.

## 속성 {#section-063be3b2f13a48a3a5ab8080718e9812}

실수, 0 이상. 회신 데이터가 생성된 이후 만료까지 남은 시간 수. 응답 이미지를 항상 즉시 만료하여 클라이언트 캐싱을 효과적으로 비활성화하려면 0으로 설정합니다. `never expire`(으)로 표시하려면 -1로 설정하십시오.

## 기본값 {#section-f55308b195c04083996f6717c8537634}

정의되지 않았거나 비어 있는 경우 `default::Expiration`에서 상속됩니다.

TTL(Time-To-Live)은 캐시가 만료되기 전 기간입니다. 기본 TTL은 10시간입니다.

## 참조 {#section-b2411d99ddb14115ad475d506efd8967}

[카탈로그::만료](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [특성::DefaultExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf), [특성::NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
