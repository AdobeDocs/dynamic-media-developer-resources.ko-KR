---
description: 요청을 성공적으로 완료할 수 없는 경우 서버는 오류 메시지와 함께 오류 이미지 또는 200이 아닌 HTTP 응답 상태를 반환합니다.
seo-description: 요청을 성공적으로 완료할 수 없는 경우 서버는 오류 메시지와 함께 오류 이미지 또는 200이 아닌 HTTP 응답 상태를 반환합니다.
seo-title: 오류
solution: Experience Manager
title: 오류
topic: Scene7 Image Serving - Image Rendering API
uuid: 5984fa9e-63c8-426b-be5f-48f66fc918c3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 오류{#errors}

요청을 성공적으로 완료할 수 없는 경우 서버는 오류 메시지와 함께 오류 이미지 또는 200이 아닌 HTTP 응답 상태를 반환합니다.

응답 상태 값은 오류 유형에 따라 달라집니다.대부분의 일반적인 오류는 &#39;403&#39;입니다. 이미지가 아닌 요청 유형에 대한 오류 응답이 와 함께 지정된 형식을 `req=`따릅니다. (현재 일관되게 구현되지 않을 수 있습니다.)

오류 메시지에 포함된 세부 정보의 양은 를 사용하여 구성할 수 `attribute::ErrorDetail`있습니다.

**오류 이미지**

이미지로 렌더링된 오류 메시지를 반환하도록 이미지 제공을 구성할 수 있습니다. 자세한 내용은 `attribute::ErrorImage` 이미지 카탈로그 참조를 참조하십시오. 오류 이미지가 성공적으로 생성되면 HTTP 응답 상태는 200입니다. 오류 이미지를 처리할 때 오류가 발생하면 표준 HTTP 오류 응답 및 텍스트 메시지가 클라이언트에 반환됩니다.

**참조**

[attribute::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b) , [attribute::ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
