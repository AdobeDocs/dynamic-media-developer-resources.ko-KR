---
description: 비이미지 응답에 대한 클라이언트 캐시 TTL입니다. 이미지가 아닌 특정 응답에 대한 만료 간격을 제공합니다.
seo-description: 비이미지 응답에 대한 클라이언트 캐시 TTL입니다. 이미지가 아닌 특정 응답에 대한 만료 간격을 제공합니다.
seo-title: NonImgExpiration
solution: Experience Manager
title: NonImgExpiration
topic: Scene7 Image Serving - Image Rendering API
uuid: 19b37bd4-f7cf-4b5f-be1a-b2d9fda5b4b1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 3%

---


# NonImgExpiration{#nonimgexpiration}

비이미지 응답에 대한 클라이언트 캐시 TTL입니다. 이미지가 아닌 특정 응답에 대한 만료 간격을 제공합니다.

다음 명령에 대한 응답으로 전송된 응답을 포함하여 특정 비이미지 응답에 대한 만료 간격을 제공합니다.

* `req=imageset`
* `req=catalogprops`
* `req=exists`
* `req=imageprops`
* `req=props`

## 속성 {#section-d37e3113f4b1468b86b5a14e80d94c83}

실수, 0 이상. 회신 데이터가 생성된 이후 만료까지 남은 시간. 응답 이미지를 항상 즉시 만료되도록 0으로 설정하면 기본 이미지 응답에 대해 클라이언트 캐싱을 효과적으로 사용할 수 없습니다. *만료되지 않음*&#x200B;으로 표시하려면 -1로 설정합니다.

## 기본값 {#section-96981360c0234b7f824d2ff7c25a7954}

정의되지 않았거나 비어 있는 경우 `default::NonImgExpiration`에서 상속됩니다.

TTL(Time-to-Live)은 캐시가 만료되기 전의 기간입니다. 기본 TTL은 6분입니다.

## 참조 {#section-4549c5594a5547beb8b129ec8d0e6aa6}

[카탈로그::만료](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) ,  [속성::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
