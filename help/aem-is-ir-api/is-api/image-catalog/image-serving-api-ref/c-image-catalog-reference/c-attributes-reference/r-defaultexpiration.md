---
description: 클라이언트 캐시 TTL을 참조하십시오. 기본 이미지 응답(defaultImage= 또는 DefaultImage 속성으로 지정된 기본 이미지를 반환하는 응답)에 대한 만료 간격을 제공합니다.
seo-description: 클라이언트 캐시 TTL을 참조하십시오. 기본 이미지 응답(defaultImage= 또는 DefaultImage 속성으로 지정된 기본 이미지를 반환하는 응답)에 대한 만료 간격을 제공합니다.
seo-title: DefaultExpiration
solution: Experience Manager
title: DefaultExpiration
topic: Scene7 Image Serving - Image Rendering API
uuid: 5266bff9-f20b-4b3b-9566-8a3f5ba0777a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# DefaultExpiration{#defaultexpiration}

클라이언트 캐시 TTL을 참조하십시오. 기본 이미지 응답에 대한 만료 간격(defaultImage= 또는 attribute::DefaultImage로 지정된 기본 이미지를 반환하는 응답)을 제공합니다.

기본 이미지가 카탈로그 레코드와 연결되지 않았거나 기본 이미지 카탈로그 레코드에 특정 `catalog::Expiration` 값이 제공되지 않는 경우에만 적용됩니다.

## 속성 {#section-e564512476604fd7b964f9f2903d6d33}

실수, 0 이상 회신 데이터가 생성된 이후 만료까지 남은 시간. 항상 응답 이미지를 즉시 만료하도록 0으로 설정하면 기본 이미지 응답에 대해 클라이언트 캐싱을 효과적으로 사용할 수 없게 됩니다. 로 `-1` 표시하도록 `never expire`설정합니다.

## 기본값 {#section-131cd32c2e214391857dba5af321f8cd}

정의되지 않았거나 비어 있는 `default::DefaultExpiration` 경우 상속됩니다.

TTL(Time-To-Live)은 캐시가 만료되기 전의 기간입니다. 기본 TTL은 1시간입니다.

## 참조 {#section-d8642c22e3d947129367dd76366963d6}

[catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-expiration-svg.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
