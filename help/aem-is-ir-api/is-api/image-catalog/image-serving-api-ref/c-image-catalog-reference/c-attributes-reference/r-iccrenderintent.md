---
title: IccRenderIntent
description: 색상 변환 렌더링 의도. 렌더링 의도에 'icc='가 지정되지 않은 경우 색상 변환에 대한 기본 렌더링 의도를 제공합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 732b1935-6556-4420-a056-4e00cb3ed152
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 4%

---

# IccRenderIntent{#iccrenderintent}

색상 변환 렌더링 의도. 렌더링 의도를 로 지정하지 않은 경우 색상 변환에 대한 기본 렌더링 의도를 제공합니다. `icc=`.

## 속성 {#section-2540099fb2fc47d29b04642da4f5922a}

열거형. 지각 0, 상대 색도계 1, 채도 2, 절대 색도계 3으로 설정합니다.

## 기본값 {#section-61a05067905b44099c228e15de279dbd}

상속 위치 `default::IccRenderIntent` 정의되지 않은 경우 또는 비어 있는 경우.

## 참조 {#section-7da9ff3038ca452a9f7375a1ca0581af}

[attribute::IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0) &#42;, [attribute::IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f), [`icc=`](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517)
