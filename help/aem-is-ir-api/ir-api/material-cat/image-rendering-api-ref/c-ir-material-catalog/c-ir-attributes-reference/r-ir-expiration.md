---
description: 기본 클라이언트 캐시 시간을 라이브로 설정합니다. 특정 카탈로그 레코드에 유효한 카탈로그 만료 또는 비네팅 만료 값이 포함되어 있지 않거나 비네팅 파일 또는 자료 파일에 카탈로그 레코드를 사용하지 않고 직접 액세스하는 경우 기본 만료 간격을 제공합니다.
solution: Experience Manager
title: 만료
feature: Dynamic Media Classic,SDK/API
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 3%

---


# 만료{#expiration}

기본 클라이언트 캐시 시간을 라이브로 설정합니다. 특정 카탈로그 레코드에 유효한 카탈로그::Expiration 또는 비네팅::Expiration 값이 포함되어 있지 않거나 비네팅 파일 또는 자료 파일이 카탈로그 레코드를 통해 액세스하는 대신 직접 액세스하는 경우 기본 만료 간격을 제공합니다.

## 속성 {#section-8e2bade105ec4905ae5c4911f500279f}

실수, 0 이상. 회신 데이터가 생성된 이후 만료까지 남은 시간. 응답 이미지를 항상 즉시 만료되도록 0으로 설정하면 클라이언트 캐싱을 효과적으로 사용할 수 없습니다. *만료되지 않음*&#x200B;으로 표시하려면 -1로 설정합니다.

## 기본값 {#section-18cfce46edb441bfae7dd9d3e0217ba9}

기본적으로 상속됨::정의되지 않았거나 비어 있는 경우 만료.

## 참조 {#section-ecfe21ff789c4b298344ebf7c647b7e7}

[카탈로그::만료](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce) ,  [비네팅::만료](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c)
