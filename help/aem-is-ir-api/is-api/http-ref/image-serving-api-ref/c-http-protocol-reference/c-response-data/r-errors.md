---
description: 요청을 성공적으로 완료할 수 없는 경우 서버는 오류 메시지와 함께 오류 이미지 또는 200 이외의 HTTP 응답 상태를 반환합니다.
solution: Experience Manager
title: 오류
feature: Dynamic Media Classic,SDK/API
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 1%

---


# 오류{#errors}

요청을 성공적으로 완료할 수 없는 경우 서버는 오류 메시지와 함께 오류 이미지 또는 200 이외의 HTTP 응답 상태를 반환합니다.

응답 상태 값은 오류 유형에 따라 달라집니다.대부분의 일반적인 오류에 대해서는 &#39;403&#39;입니다. 이미지가 아닌 요청 유형에 대한 오류 응답은 `req=`에 지정된 형식을 따릅니다. (현재 일관성 있게 구현되지 않을 수 있습니다.)

오류 메시지에 포함된 세부 정보의 양은 `attribute::ErrorDetail`으로 구성할 수 있습니다.

## 오류 이미지 {#section-92e9b20b2507433daa96923abc95f777}

이미지에 렌더링된 오류 메시지를 반환하도록 이미지 제공을 구성할 수 있습니다.

자세한 내용은 이미지 카탈로그 참조에서 [attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c)을 참조하십시오.

오류 이미지가 성공적으로 생성되면 HTTP 응답 상태는 200입니다. 오류 이미지를 처리할 때 오류가 발생하면 표준 HTTP 오류 응답 및 텍스트 메시지가 클라이언트에 반환됩니다.

## 기본 이미지 {#section-66bf25fe6b434081bfae96d38d9be25e}

누락된 이미지를 기본 이미지로 대체하도록 이미지 제공을 구성할 수 있습니다. 기본 이미지는 `attribute::DefaultImage` 또는 `defaultImage=` 명령으로 지정할 수 있습니다.

## 참조 {#section-e261d7f224ca4546bb64bf8cb909db08}

[속성::ErrorDetail](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561) ,  [속성::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c),  [속성::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433),  [defaultImage=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-defaultimage.md#reference-209aa6ce830f490483412eb26af67fd2)
