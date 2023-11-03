---
description: 요청을 성공적으로 완료할 수 없는 경우 서버는 오류 메시지와 함께 오류 이미지 또는 200 이외의 HTTP 응답 상태를 반환합니다.
solution: Experience Manager
title: 오류
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9314782f-703b-4e9c-a026-62970d1c752f
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 2%

---

# 오류{#errors}

요청을 성공적으로 완료할 수 없는 경우 서버는 오류 메시지와 함께 오류 이미지 또는 200 이외의 HTTP 응답 상태를 반환합니다.

응답 상태 값은 오류 유형에 따라 다릅니다. 대부분의 일반적인 오류의 경우 &#39;403&#39;입니다. 이미지가 아닌 요청 유형에 대한 오류 응답은 `req=`. (현재 일관되게 구현되지 않을 수 있습니다.)

오류 메시지에 포함된 세부 정보의 양은 `attribute::ErrorDetail`.

## 오류 이미지 {#section-92e9b20b2507433daa96923abc95f777}

이미지 제공은 이미지에 렌더링된 오류 메시지를 반환하도록 구성할 수 있습니다.

다음을 참조하십시오 [attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c) 자세한 내용은 이미지 카탈로그 참조 를 참조하십시오.

오류 이미지가 성공적으로 생성되면 HTTP 응답 상태는 200입니다. 오류 이미지를 처리할 때 오류가 발생하면 표준 HTTP 오류 응답 및 텍스트 메시지가 클라이언트에 반환됩니다.

## 기본 이미지 {#section-66bf25fe6b434081bfae96d38d9be25e}

이미지 제공은 누락된 이미지를 기본 이미지로 대체하도록 구성할 수 있습니다. 기본 이미지는 다음 중 하나를 사용하여 지정할 수 있습니다. `attribute::DefaultImage` 또는 `defaultImage=` 명령입니다.

## 참조 {#section-e261d7f224ca4546bb64bf8cb909db08}

[attribute::ErrorDetail](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561) , [attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c), [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433), [defaultImage=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-defaultimage.md#reference-209aa6ce830f490483412eb26af67fd2)
