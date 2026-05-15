---
description: 이미지 크기. 카탈로그 경로에서 참조하는 전체 해상도 이미지의 픽셀 크기입니다.
solution: Experience Manager
title: 크기
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 46f06cbb-d70f-4334-966c-624b49c3bb9b
TQID: 'https://experienceleague.adobe.com/wS28XEIvINBBoYZSI-frpSbCikCyC5AhT6TyDgMsGFg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 108
ht-degree: 5%

---

# 크기{#size}

이미지 크기. catalog::Path에서 참조한 전체 해상도 이미지의 픽셀 크기입니다.

이 값이 제공되면 이미지 제공에서는 실제 이미지 크기를 얻기 위해 이미지를 열 필요가 없도록 이 값을 사용합니다.

>[!NOTE]
>
>`catalog::Size`이(가) 제공되고 실제 전체 해상도 이미지 크기와 같지 않으면 정의되지 않은 동작이 발생할 수 있습니다.

## 속성 {#section-5c914ec8b1444a8e99d811b647cd42a3}

각각 0보다 큰 두 개의 정수를 쉼표로 구분합니다. 선택적.

## 기본값 {#section-257c6d47cf314ef0b3c3c32b18f0f0f1}

필드가 없거나 필드가 비어 있는 경우 이미지의 실제 크기가 사용됩니다.

## 참조 {#section-e63797357d5a4119a10db1e6e088f6e9}

[카탈로그::경로](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c) , [res=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md)
