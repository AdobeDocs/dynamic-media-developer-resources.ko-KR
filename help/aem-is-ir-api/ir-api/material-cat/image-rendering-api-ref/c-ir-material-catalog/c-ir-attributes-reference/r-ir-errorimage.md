---
title: 오류 이미지
description: 오류 응답 이미지입니다. 이미지 렌더링은 일반적으로 오류가 발생할 때 텍스트 메시지와 함께 오류 상태를 반환합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ed48482f-79b0-4c81-b5cd-cf997f27d3ab
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 1%

---

# 오류 이미지 {#errorimage}

오류 응답 이미지입니다. 이미지 렌더링은 일반적으로 오류가 발생할 때 텍스트 메시지와 함께 오류 상태를 반환합니다. 다음 `attribute::ErrorImage` 오류가 있는 경우 이미지를 반환하도록 구성할 수 있습니다.

오류가 발생하면 서버는 다음 값 해석을 시도합니다. `ImageRendering::attribute::ErrorImage`를 단순 이미지 파일 경로로 사용합니다. 파일을 열 수 없을 경우에는에 설명된 대로 처리되는 이미지 제공에 속성 값과 오류 세부 정보를 보냅니다. `ImageServing::attribute::ErrorImage`. 이미지 제공이 유효한 응답 이미지를 반환하지 않으면 표준 HTTP 오류 상태와 텍스트 메시지가 클라이언트에 전송됩니다.

오류 이미지가 HTTP 상태 200으로 반환됩니다.

## 속성 {#section-4a4a7e37ed11483db0b9922dc68ea7db}

텍스트 문자열입니다. 지정하면 다음 중 하나여야 합니다. **`ImageServing::catalog::id`** 값, 상대 경로(대상) **`ImageServing::attribute::RootPath`** 또는 **`ImageRendering::attribute::RootPath`**&#x200B;이미지 서버에서 액세스할 수 있는 이미지 파일의 절대 경로입니다.

## 기본값 {#section-4c463e369dfb4b43a7b2a3bce9619dd4}

상속 위치 `default::ErrorImage` 정의되지 않은 경우 정의되어 있지만 비어 있는 경우, 다음과 같은 경우에도 오류 이미지 동작이 비활성화됩니다. `default::ErrorImage` 가 정의되어 있고 HTTP 오류 상태가 반환됩니다.

## 참조 {#section-3e0308eaf4124451909dacd570e27695}

[attribute::DefaultImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f), [attribute::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b), [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3), [catalog::Id](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-id.md#reference-cba2a53a952e403fb57a4e8569f9cf85)
