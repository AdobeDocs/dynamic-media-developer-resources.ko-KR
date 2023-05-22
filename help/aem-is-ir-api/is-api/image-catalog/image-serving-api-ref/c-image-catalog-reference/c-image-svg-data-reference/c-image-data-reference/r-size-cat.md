---
description: 이미지 크기. 카탈로그 경로에서 참조하는 전체 해상도 이미지의 픽셀 크기입니다.
solution: Experience Manager
title: 크기
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 46f06cbb-d70f-4334-966c-624b49c3bb9b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 9%

---

# 크기{#size}

이미지 크기. catalog::Path에서 참조한 전체 해상도 이미지의 픽셀 크기입니다.

이 값이 제공되면 이미지 제공에서는 실제 이미지 크기를 얻기 위해 이미지를 열 필요가 없도록 이 값을 사용합니다.

>[!NOTE]
>
>If `catalog::Size`가 제공되며 실제 전체 해상도 이미지 크기와 동일하지 않으므로 정의되지 않은 동작이 발생할 수 있습니다.

## 속성 {#section-5c914ec8b1444a8e99d811b647cd42a3}

각각 0보다 큰 두 개의 정수를 쉼표로 구분합니다. 선택적.

## 기본값 {#section-257c6d47cf314ef0b3c3c32b18f0f0f1}

필드가 없거나 필드가 비어 있는 경우 이미지의 실제 크기가 사용됩니다.

## 참조 {#section-e63797357d5a4119a10db1e6e088f6e9}

[catalog::Path](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c) , [res=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md)
