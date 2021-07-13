---
description: ID
solution: Experience Manager
title: ID
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d7b37180-cc93-41cd-bf14-5c262b046fbc
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 5%

---

# ID{#id}

일반적으로 SKU 번호와 같은 짧고 고유한 식별자로, SKU에 여러 이미지가 있거나 로케일 특정 변형을 포함하는 경우와 같이 일부 접미사가 있을 수 있습니다. 또한 이미지 제공 기능을 통해 웹 사이트를 손쉽게 재시작할 수 있도록 파일 경로와 유사하게 보이는 보다 복잡한 문자열일 수 있습니다.

>[!NOTE]
>
>이미지 카탈로그가 로드되면 이미지 및 SVG 테이블이 단일 테이블로 병합됩니다. Id 값은 두 테이블에서 고유해야 합니다. 이미지 테이블에 동일한 ID 값이 있는 레코드가 포함된 경우 SVG 레코드가 삭제됩니다. 정적 콘텐츠는 별도의 표로 관리됩니다. 정적 콘텐츠 항목 및 이미지/SVG 항목에 동일한 ID 값이 있을 수 있습니다.

## 속성 {#section-874a6853f67b4b229341ca76682884ae}

텍스트 문자열입니다. 필수. 이미지/SVG 또는 정적 콘텐츠 데이터 테이블에 대한 식별자를 기록합니다. 이 이미지 카탈로그/SVG 카탈로그 또는 이 정적 콘텐츠 카탈로그 내의 각 `catalog::Id` 값은 고유해야 하며 &#39;,&#39; 문자를 포함하지 않아야 합니다.

## 기본값 {#section-a26e7d83a5ee44b5918baef82ee48e14}

없음.

## 참조 {#section-a258d818487d4ee6b7a99a65d18471a9}

[attribute::RootId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546)
