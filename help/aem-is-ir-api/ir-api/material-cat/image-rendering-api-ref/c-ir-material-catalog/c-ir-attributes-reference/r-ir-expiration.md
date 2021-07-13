---
description: 기본 클라이언트 캐시 사용 시간입니다. 특정 카탈로그 레코드에 유효한 카탈로그 만료 또는 비네팅 만료 값이 없거나 비네팅 파일 또는 자료 파일에 카탈로그 레코드를 통해 액세스하는 경우가 아닌 경우 기본 만료 간격을 제공합니다.
solution: Experience Manager
title: 만료
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6d9cca06-f675-4ae4-a187-9cd716e7c554
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 3%

---

# 만료{#expiration}

기본 클라이언트 캐시 사용 시간입니다. 특정 카탈로그 레코드에 유효한 카탈로그:Expiration 또는 vignette::Expiration 값이 없거나 비네팅 파일 또는 재료 파일이 카탈로그 레코드를 통해서가 아니라 직접 액세스하는 경우 기본 만료 간격을 제공합니다.

## 속성 {#section-8e2bade105ec4905ae5c4911f500279f}

실수, 0 이상 회신 데이터가 생성된 이후 만료까지 남은 시간 항상 회신 이미지를 즉시 만료하려면 0으로 설정하여 클라이언트 캐싱을 효과적으로 사용하지 않도록 설정합니다. *만료되지 않음*&#x200B;으로 표시하려면 -1로 설정하십시오.

## 기본값 {#section-18cfce46edb441bfae7dd9d3e0217ba9}

기본값에서 상속됨::정의되지 않았거나 비어 있는 경우 만료입니다.

## 참조 {#section-ecfe21ff789c4b298344ebf7c647b7e7}

[카탈로그::만료](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce) ,  [비네팅::만료](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c)
