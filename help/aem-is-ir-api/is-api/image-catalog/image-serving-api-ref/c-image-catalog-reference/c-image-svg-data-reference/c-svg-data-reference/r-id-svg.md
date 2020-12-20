---
description: 널
seo-description: 널
seo-title: ID
solution: Experience Manager
title: ID
topic: Scene7 Image Serving - Image Rendering API
uuid: a700472c-e1eb-4eb0-95ff-7afd4ce27931
translation-type: tm+mt
source-git-commit: 7721cccf3f779f258adcdcf886f7e01111e92be0
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 6%

---


# ID{#id}

일반적으로 SKU에 이미지가 여러 개 있거나 로케일별 차이가 있는 경우와 같이 SKU 번호와 같은 짧고 고유한 식별자입니다. 또한 이미지 제공 기능을 사용하여 웹 사이트를 쉽게 재배치할 수 있도록 파일 경로와 유사하게 보이는 보다 복잡한 문자열일 수 있습니다.

>[!NOTE]
>
>이미지 카탈로그가 로드되면 이미지와 SVG 표가 단일 테이블로 병합됩니다. ID 값은 두 표 모두에서 고유해야 합니다. 이미지 테이블에 ID 값이 동일한 레코드가 포함된 경우 SVG 레코드가 무시됩니다. 정적 컨텐츠는 별도의 테이블로 관리됩니다.정적 컨텐츠 항목 및 이미지/SVG 항목의 ID 값이 같을 수 있습니다.

## 속성 {#section-874a6853f67b4b229341ca76682884ae}

텍스트 문자열. 필수. 이미지/SVG 또는 정적 컨텐츠 데이터 테이블에 대한 식별자를 기록합니다. 이 이미지 카탈로그/SVG 카탈로그 또는 이 정적 컨텐츠 카탈로그 내의 각 `catalog::Id` 값은 고유해야 하며 &#39;,&#39; 문자를 포함할 수 없습니다.

## 기본값 {#section-a26e7d83a5ee44b5918baef82ee48e14}

없음.

## 참조 {#section-a258d818487d4ee6b7a99a65d18471a9}

[특성::RootId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546)
