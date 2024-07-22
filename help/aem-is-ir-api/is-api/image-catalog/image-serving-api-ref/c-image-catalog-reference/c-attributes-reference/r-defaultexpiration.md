---
description: 기본 이미지 응답을 위한 클라이언트 캐시 TTL. 기본 이미지 응답(defaultImage= 또는 특성 DefaultImage로 지정된 기본 이미지를 반환하는 응답)에 대한 만료 간격을 제공합니다.
solution: Experience Manager
title: DefaultExpiration
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 99103681-c00c-4648-8dee-2314e7e614af
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 1%

---

# DefaultExpiration{#defaultexpiration}

기본 이미지 응답을 위한 클라이언트 캐시 TTL. 기본 이미지 응답(defaultImage= 또는 attribute::DefaultImage로 지정된 기본 이미지를 반환하는 응답)에 대한 만료 간격을 제공합니다.

기본 이미지가 카탈로그 레코드와 연결되어 있지 않거나 기본 이미지 카탈로그 레코드가 특정 `catalog::Expiration` 값을 제공하지 않는 경우에만 적용됩니다.

## 속성 {#section-e564512476604fd7b964f9f2903d6d33}

실수, 0 이상. 회신 데이터가 생성된 이후 만료까지 남은 시간 수. 응답 이미지를 항상 즉시 만료하려면 0으로 설정하면 기본 이미지 응답에 대한 클라이언트 캐싱이 효과적으로 비활성화됩니다. `never expire`(으)로 표시하려면 `-1`(으)로 설정합니다.

## 기본값 {#section-131cd32c2e214391857dba5af321f8cd}

정의되지 않았거나 비어 있는 경우 `default::DefaultExpiration`에서 상속됩니다.

TTL(Time-To-Live)은 캐시가 만료되기 전 기간입니다. 기본 TTL은 1시간입니다.

## 참조 {#section-d8642c22e3d947129367dd76366963d6}

[카탈로그::만료](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-expiration-svg.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [특성::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
