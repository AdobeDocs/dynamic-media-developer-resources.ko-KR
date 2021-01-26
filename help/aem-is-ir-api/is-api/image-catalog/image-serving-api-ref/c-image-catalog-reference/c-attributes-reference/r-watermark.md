---
description: 워터마크 선택기. 워터마크 이미지 또는 템플릿으로 사용할 카탈로그 레코드의 카탈로그 ID를 지정합니다.
seo-description: 워터마크 선택기. 워터마크 이미지 또는 템플릿으로 사용할 카탈로그 레코드의 카탈로그 ID를 지정합니다.
seo-title: 워터마크
solution: Experience Manager
title: 워터마크
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 18add7ab-0797-4ab3-a7e8-05c745abe605
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 5%

---


# 워터마크{#watermark}

워터마크 선택기. 워터마크 이미지 또는 템플릿으로 사용할 카탈로그 레코드의 카탈로그::Id를 지정합니다.

지정된 경우 서버는 모든 이미지 요청에 대해 요청된 이미지 데이터에 워터마크를 적용합니다( `req=img`).

## 속성 {#section-fad6ffff4c5f4b5c8010281bc1377055}

텍스트 문자열. 지정된 경우 이 이미지 카탈로그의 유효한 `Catalog::Id` 값이거나 [!DNL default.ini]에 지정된 경우 기본 카탈로그에 있어야 합니다.

## 기본값 {#section-f8a2029b5b8740b2af149bdbfa28fbae}

정의되지 않은 경우 `default::Watermark`에서 상속됩니다. `default::Watermark`이(가) 정의되어 있어도 이 이미지 카탈로그에 워터마크가 적용되지 않습니다.

## 참조 {#section-f15dbe31013849828d78588742dde58e}

[카탈로그::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
