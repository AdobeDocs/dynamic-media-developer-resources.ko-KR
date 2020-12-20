---
description: 이미지 크기. 카탈로그 경로에서 참조하는 전체 해상도 이미지의 픽셀 크기입니다.
seo-description: 이미지 크기. 카탈로그 경로에서 참조하는 전체 해상도 이미지의 픽셀 크기입니다.
seo-title: 크기
solution: Experience Manager
title: 크기
topic: Scene7 Image Serving - Image Rendering API
uuid: 6fe2aeb6-0dd7-4631-955f-ad74d11b613d
translation-type: tm+mt
source-git-commit: b4331c6f033903ec64f168da0b739927c6066710
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 11%

---


# 크기{#size}

이미지 크기. 카탈로그::Path에서 참조하는 전체 해상도 이미지의 픽셀 크기입니다.

이 값이 제공되면 이미지 제공에서는 실제 이미지 크기를 얻기 위해 이미지를 열지 않고도 이 값을 사용합니다.

>[!NOTE]
>
>`catalog::Size`이(가) 제공되어 실제 전체 해상도 이미지 크기와 동일하지 않으면 정의되지 않은 동작이 발생할 수 있습니다.

## 속성 {#section-5c914ec8b1444a8e99d811b647cd42a3}

각각 0보다 큰 정수 2개를 쉼표로 구분하여 입력합니다. 선택 사항입니다.

## 기본값 {#section-257c6d47cf314ef0b3c3c32b18f0f0f1}

필드가 없거나 필드가 비어 있으면 이미지의 실제 크기가 사용됩니다.

## 참조 {#section-e63797357d5a4119a10db1e6e088f6e9}

[catalog::Path](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c) ,  [res=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md)
