---
title: 만료
description: 기본 클라이언트 캐시 TTL(Time to Live).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6d9cca06-f675-4ae4-a187-9cd716e7c554
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 4%

---

# 만료{#expiration}

기본 클라이언트 캐시 TTL(Time to Live). 특정 카탈로그 레코드에 유효한 만료 간격이 없는 경우 기본 만료 간격을 제공합니다. `catalog::Expiration` 또는 `vignette::Expiration` 값. 또는 카탈로그 레코드가 아닌 비네팅 파일 또는 자료 파일에 직접 액세스하는 경우.

## 속성 {#section-8e2bade105ec4905ae5c4911f500279f}

실수, `0` 또는 그 이상 회신 데이터가 생성된 이후 만료까지 남은 시간 수. 다음으로 설정 `0` 응답 이미지를 항상 즉시 만료하여 클라이언트 캐싱을 효과적으로 비활성화합니다. 다음으로 설정 `-1` 로 표시 *만료 기간 제한 없음*.

## 기본값 {#section-18cfce46edb441bfae7dd9d3e0217ba9}

상속 위치 `default::Expiration` 정의되지 않은 경우 또는 비어 있는 경우.

## 참조 {#section-ecfe21ff789c4b298344ebf7c647b7e7}

[catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce) , [비네팅::만료](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c)
