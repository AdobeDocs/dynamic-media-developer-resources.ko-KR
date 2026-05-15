---
title: IccRenderIntent
description: 색상 변환 렌더링 의도. 렌더링 의도에 'icc='가 지정되지 않은 경우 색상 변환에 대한 기본 렌더링 의도를 제공합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 732b1935-6556-4420-a056-4e00cb3ed152
TQID: 'https://experienceleague.adobe.com/r9OiAkf9-hGubl8id7-ZkN3K-tpzhBc73utDU7doxZM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 77
ht-degree: 3%

---

# IccRenderIntent{#iccrenderintent}

색상 변환 렌더링 의도. 렌더링 의도가 `icc=`에 지정되어 있지 않은 경우 색상 변환에 대한 기본 렌더링 의도를 제공합니다.

## 속성 {#section-2540099fb2fc47d29b04642da4f5922a}

열거형. 지각 0, 상대 색도계 1, 채도 2, 절대 색도계 3으로 설정합니다.

## 기본값 {#section-61a05067905b44099c228e15de279dbd}

정의되지 않았거나 비어 있는 경우 `default::IccRenderIntent`에서 상속됩니다.

## 참조 {#section-7da9ff3038ca452a9f7375a1ca0581af}

[특성::IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0) &#42;, [특성::IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f), [`icc=`](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517)
