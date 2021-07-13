---
description: 비이미지 응답에 대한 클라이언트 캐시 TTL입니다. 특정 비이미지 응답에 대한 만료 간격을 제공합니다.
solution: Experience Manager
title: NonImgExpiration
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c61e2781-dfaa-4f3d-958d-5ffa755a3e4d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 3%

---

# NonImgExpiration{#nonimgexpiration}

비이미지 응답에 대한 클라이언트 캐시 TTL입니다. 특정 비이미지 응답에 대한 만료 간격을 제공합니다.

다음 명령에 대한 응답으로 전송된 응답을 포함하여 특정 비이미지 응답에 대한 만료 간격을 제공합니다.

* `req=imageset`
* `req=catalogprops`
* `req=exists`
* `req=imageprops`
* `req=props`

## 속성 {#section-d37e3113f4b1468b86b5a14e80d94c83}

실수, 0 이상 회신 데이터가 생성된 이후 만료까지 남은 시간 항상 회신 이미지를 즉시 만료하려면 0으로 설정하면 기본 이미지 응답에 대해 클라이언트 캐싱을 효과적으로 비활성화할 수 있습니다. *만료되지 않음*&#x200B;으로 표시하려면 -1로 설정하십시오.

## 기본값 {#section-96981360c0234b7f824d2ff7c25a7954}

정의되지 않았거나 비어 있는 경우 `default::NonImgExpiration`에서 상속됩니다.

TTL(Time-To-Live)은 캐시가 만료되기 전의 기간입니다. 기본 TTL은 6분입니다.

## 참조 {#section-4549c5594a5547beb8b129ec8d0e6aa6}

[카탈로그::만료](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) ,  [속성::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
