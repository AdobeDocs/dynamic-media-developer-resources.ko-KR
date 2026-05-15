---
description: 정적 콘텐츠 카탈로그 데이터 파일 경로. 이 카탈로그의 정적 콘텐츠 데이터를 포함하는 파일을 지정합니다.
solution: Experience Manager
title: StaticContentCatalogFile
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ff6f0ad8-189f-4172-89cb-f138d2df8fe4
TQID: 'https://experienceleague.adobe.com/98uNzMz83z3lfa2d3LNixYKZzUWWE9zqrK1fnPo-JNA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 116
ht-degree: 3%

---

# StaticContentCatalogFile{#staticcontentcatalogfile}

정적 콘텐츠 카탈로그 데이터 파일 경로. 이 카탈로그의 정적 콘텐츠 데이터를 포함하는 파일을 지정합니다.

정적 콘텐츠 카탈로그 데이터 파일은 지정된 순서대로 로드됩니다. 동일한 `static::Id` 값이 두 개 이상의 레코드(동일한 카탈로그 파일 또는 다른 카탈로그 파일)에 있으면 마지막 인스턴스가 우세합니다.

## 속성 {#section-3f8dc8d21fa84fbeb71db6ca1ecbdd8c}

쉼표로 구분된 하나 이상의 텍스트 문자열 값. 선택적. 각 값은 카탈로그 폴더에 상대적인 절대 파일 경로 또는 경로여야 합니다.

## 기본값 {#section-702edfbc00c54fc29e412a3ff99fef2b}

비어 있음 - 이 이미지 카탈로그에 정적 콘텐츠 데이터가 포함되지 않음을 나타냅니다.

## 참조 {#section-13d78d475fff40e7a4edf9a9c73f3c15}

[카탈로그 데이터](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
