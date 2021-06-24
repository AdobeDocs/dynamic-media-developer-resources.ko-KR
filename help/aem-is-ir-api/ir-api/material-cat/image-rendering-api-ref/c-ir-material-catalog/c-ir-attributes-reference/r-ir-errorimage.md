---
description: 오류 응답 이미지입니다. 이미지 렌더링은 일반적으로 오류가 발생할 때 텍스트 메시지와 함께 오류 상태를 반환합니다. errorImage 속성을 사용하면 오류가 발생할 경우 이미지를 구성할 수 있습니다.
solution: Experience Manager
title: ErrorImage *
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: ed48482f-79b0-4c81-b5cd-cf997f27d3ab
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 1%

---

# ErrorImage *{#errorimage}

오류 응답 이미지입니다. 이미지 렌더링은 일반적으로 오류가 발생할 때 텍스트 메시지와 함께 오류 상태를 반환합니다. attribute::ErrorImage를 사용하면 오류가 발생하는 경우 이미지를 구성할 수 있습니다.

오류가 발생하면 서버는 먼저 `ImageRendering::attribute::ErrorImage`의 값을 단순 이미지 파일 경로로 해석하려고 합니다. 파일을 열 수 없으면 `ImageServing::attribute::ErrorImage`에 설명된 대로 처리하는 Image Serving으로 속성 값과 오류 세부 정보를 보냅니다. 이미지 제공 기능이 유효한 응답 이미지를 반환하지 않으면 표준 HTTP 오류 상태 및 텍스트 메시지가 클라이언트에 전송됩니다.

오류 이미지가 HTTP 상태 200과 함께 반환됩니다.

## 속성 {#section-4a4a7e37ed11483db0b9922dc68ea7db}

텍스트 문자열입니다. 지정하면, **`ImageServing::catalog::id`** 값, 상대 경로(**`ImageServing::attribute::RootPath`** 또는 **`ImageRendering::attribute::RootPath`**&#x200B;에 대한 경로) 또는 이미지 서버에서 액세스할 수 있는 이미지 파일의 절대 경로여야 합니다.

## 기본값 {#section-4c463e369dfb4b43a7b2a3bce9619dd4}

정의되지 않은 경우 `default::ErrorImage`에서 상속됩니다. 이 값이 정의되어 있지만 비어 있으면 `default::ErrorImage` 이 정의되어 있고 HTTP 오류 상태가 반환되더라도 오류 이미지 동작이 비활성화됩니다.

## 참조 {#section-3e0308eaf4124451909dacd570e27695}

[attribute::DefaultImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f),  [attribute::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b),  [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3),  [catalog::Id](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-id.md#reference-cba2a53a952e403fb57a4e8569f9cf85)
