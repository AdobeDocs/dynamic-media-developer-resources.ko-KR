---
title: Id
description: 일반적으로 SKU 번호와 같은 짧고 고유한 식별자는 SKU에 여러 이미지가 있거나 로케일별 변형이 있는 경우와 같이 일종의 접미사가 있을 수 있습니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 818649dd-bcb7-4ff5-9308-6b5dc06f66e1
source-git-commit: c1a4dad7888d31e0b78f0fc5091700ad8104e685
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 2%

---

# Id{#id}

일반적으로 SKU 번호와 같은 짧고 고유한 식별자는 SKU에 여러 이미지가 있거나 로케일별 변형이 있는 경우와 같이 일부 종류의 접미사가 있을 수 있습니다. 또한 이미지 제공으로 웹 사이트를 쉽게 리모델링할 수 있도록 지원하기 위해 파일 경로처럼 보이는 보다 복잡한 문자열일 수 있습니다.

>[!NOTE]
>
>이미지 카탈로그가 로드되면 이미지 및 SVG 테이블이 단일 테이블로 병합됩니다. 두 테이블 모두에서 ID 값이 고유해야 합니다. 이미지 테이블에 동일한 ID 값을 가진 레코드가 포함되어 있으면 SVG 레코드가 무시됩니다. 정적 콘텐츠는 별도의 테이블로 관리됩니다. 따라서 정적 콘텐츠 항목과 이미지/SVG 항목은 동일한 ID 값을 가질 수 있습니다.

## 속성 {#section-874a6853f67b4b229341ca76682884ae}

텍스트 문자열입니다. 필수. 이미지/SVG 또는 정적 컨텐츠 데이터 테이블에 대한 레코드 식별자입니다. 각 `catalog::Id` 이 이미지 카탈로그/SVG 카탈로그 내 또는 이 정적 콘텐츠 카탈로그 내 값은 고유해야 하며 &#39;,&#39; 문자를 포함하지 않아야 합니다.

## 기본값 {#section-a26e7d83a5ee44b5918baef82ee48e14}

없음.

## 참조 {#section-a258d818487d4ee6b7a99a65d18471a9}

[attribute::RootId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546)
