---
description: 만료
solution: Experience Manager
title: 만료
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 2%

---


# 만료{#expiration}

클라이언트 및 프록시 서버 캐싱을 관리하는 데 사용됩니다. 서버는 이 값을 전송 시간/날짜에 추가하여 HTTP 응답 데이터의 만료 시간/날짜를 계산합니다.

브라우저는 파일의 만료 시간을 사용하여 캐시를 관리합니다. 서버에 요청을 전달하기 전에 브라우저는 해당 캐시를 확인하여 파일이 이미 다운로드되었는지 확인합니다. 이 경우, 그리고 파일이 아직 만료되지 않은 경우, 브라우저는 일반 GET 요청 대신 조건부 GET 요청을 보냅니다(예: 요청 헤더에 If-Modified-Since 필드가 설정된 경우). 서버에는 &#39;304&#39; 상태로 응답하고 이미지를 전송하지 않는 옵션이 있습니다. 그런 다음 브라우저는 캐시에서 파일을 로드합니다. 이렇게 하면 자주 액세스하는 데이터의 전체 성능이 크게 향상될 수 있습니다.

만료는 다음 응답 유형에 사용됩니다.

* `req=img`
* `req=mask`
* `req=tmb`
* `req=userdata`
* `req=map`

특정 유형의 응답(예: 오류 응답)은 항상 즉시 만료되도록 표시되거나(또는 액세스가 불가능으로 태그 지정됨), 다른 응답(예: 속성 또는 기본 이미지 응답)은 특수 만료 설정( `attribute::NonImgExpiration` 및 `attribute::DefaultExpiration`)을 사용합니다.

## 속성 {#section-7f5173d090cf48df8fa1a2c72b8c8c60}

실수, -2, -1 또는 0 이상. 응답 이미지가 생성된 이후 만료까지 남은 시간. 응답 이미지를 항상 즉시 만료되도록 0으로 설정하면 클라이언트 캐싱을 효과적으로 사용할 수 없습니다. *`never expire`*&#x200B;으로 표시하려면 -1로 설정합니다. 이 경우 서버는 파일이 실제로 변경되었는지 여부를 확인하지 않고 조건부 GET 요청에 응답하여 항상 304 상태(수정되지 않음)를 반환합니다. `attribute::Expiration`에서 제공하는 기본값을 사용하려면 -2로 설정합니다.

## 기본값 {#section-ec72cc1dfc5e4f278174d37da2e39462}

`attribute::Expiration` 값이 -2인 경우, 또는 필드가 비어 있는 경우에 사용됩니다.

## 참조 {#section-0e5e8595aad641c689726828712a8902}

[특성::Expiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-expiration.md#reference-a0bf4686425d4e00b8014c4950fb62b7),  [특성::DefaultExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf),  [속성::NonImgExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d),  [req=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
