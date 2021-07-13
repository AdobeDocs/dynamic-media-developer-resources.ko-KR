---
description: 요청을 성공적으로 완료할 수 없으면 서버에서 오류 이미지 또는 오류 메시지와 함께 200 이외의 HTTP 응답 상태를 반환합니다.
solution: Experience Manager
title: 오류
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e45e3968-3659-470b-a88a-fe7ba73d8207
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 2%

---

# 오류{#errors}

요청을 성공적으로 완료할 수 없으면 서버에서 오류 이미지 또는 오류 메시지와 함께 200 이외의 HTTP 응답 상태를 반환합니다.

응답 상태 값은 오류 유형에 따라 달라집니다. 대부분의 일반적인 오류의 경우 &#39;403&#39;입니다. 이미지가 아닌 요청 유형에 대한 오류 응답이 `req=`에 지정된 형식을 따릅니다. (현재 일관되게 구현되지 않을 수 있습니다.)

오류 메시지에 포함된 세부 정보의 양은 `attribute::ErrorDetail`으로 구성할 수 있습니다.

**오류 이미지**

이미지에 렌더링된 오류 메시지를 반환하도록 이미지 제공 기능을 구성할 수 있습니다. 자세한 내용은 이미지 카탈로그 참조에서 `attribute::ErrorImage` 을 참조하십시오. 오류 이미지가 성공적으로 생성되면 HTTP 응답 상태는 200입니다. 오류 이미지를 처리할 때 오류가 발생하면 표준 HTTP 오류 응답 및 텍스트 메시지가 클라이언트에 반환됩니다.

**참조**

[attribute::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b) ,  [attribute::ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
