---
description: 클라이언트의 실시간 캐시 시간 만료까지 남은 시간. 클라이언트 및 프록시 서버 캐싱을 관리하는 데 사용됩니다.
seo-description: 클라이언트의 실시간 캐시 시간 만료까지 남은 시간. 클라이언트 및 프록시 서버 캐싱을 관리하는 데 사용됩니다.
seo-title: 만료
solution: Experience Manager
title: 만료
topic: Scene7 Image Serving - Image Rendering API
uuid: 6dbd7d43-727c-42fc-8953-dba112209a45
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 2%

---


# 만료{#expiration}

클라이언트의 실시간 캐시 시간 만료까지 남은 시간. 클라이언트 및 프록시 서버 캐싱을 관리하는 데 사용됩니다.

서버는 이 값을 전송 시간/날짜에 추가하여 NTTP 응답 데이터의 만료 시간/날짜를 계산합니다.

브라우저는 파일의 만료 시간을 사용하여 캐시를 관리합니다. 서버에 요청을 전달하기 전에 브라우저가 해당 캐시를 확인하여 파일이 이미 다운로드되었는지 확인합니다. 이 경우, 그리고 파일이 아직 만료되지 않은 경우, 브라우저는 일반 GET 요청 대신 조건부 GET 요청(예: 수정된 경우-이후 HTTP 요청 헤더)을 보냅니다. 서버에는 &#39;304&#39; 상태로 응답하고 이미지를 전송하지 않는 옵션이 있습니다. 그러면 브라우저는 캐시에서 파일을 간단히 로드합니다. 이렇게 하면 자주 액세스하는 데이터의 전체 성능이 크게 향상될 수 있습니다.

서버에서 만료 HTTP 응답 헤더를 현재 날짜/시간과 가장 작은 비네팅::Expiration 및 모든 카탈로그::비네팅에 대한 만료 값 및 렌더링 작업에 관련된 모든 자료를 설정합니다.

만료는 주로 이미지 데이터 응답에 대해 설정됩니다. 모든 오류 응답 또는 속성 응답을 포함하여 특정 유형의 응답은 항상 즉시 만료(또는 액세스가 불가능으로 태그 지정됨)로 표시됩니다.

## 속성 {#section-e87e8f6b6d224c6ea2eeaad695c04be8}

실수, -2, -1, 0 이상. 응답 이미지가 생성된 이후 만료까지 남은 시간. 응답 이미지를 항상 즉시 만료되도록 0으로 설정하면 클라이언트 캐싱을 효과적으로 사용할 수 없습니다. `never expire`으로 표시하려면 -1로 설정합니다. 이 경우 서버는 파일이 실제로 변경되었는지 여부를 확인하지 않고 조건부 `GET` 요청에 응답하여 항상 304 상태(수정되지 않음)를 반환합니다. `attribute::Expiration`에서 제공하는 기본값을 사용하려면 -2로 설정합니다.

## 기본값 {#section-79d71706e12a4493a69d7febc3a1f271}

`attribute::Expiration` 값이 -2인 경우, 또는 필드가 비어 있는 경우에 사용됩니다.

## 참조 {#section-9d46a9d346fe42f3911edb3bd79f4121}

[속성::만료](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996) ,  [비네팅::만료](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c),  [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
