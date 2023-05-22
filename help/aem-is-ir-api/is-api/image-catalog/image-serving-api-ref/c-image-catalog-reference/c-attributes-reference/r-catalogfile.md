---
description: 이미지 데이터 파일 경로. 이 카탈로그의 이미지 데이터를 포함하는 파일을 지정합니다.
solution: Experience Manager
title: 카탈로그 파일
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 240a3884-68dd-474c-83a6-d79fc5b6c300
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 3%

---

# 카탈로그 파일{#catalogfile}

이미지 데이터 파일 경로. 이 카탈로그의 이미지 데이터를 포함하는 파일을 지정합니다.

이미지 데이터 파일은 지정된 순서대로 로드됩니다. 동일한 경우 `catalog::Id` 값이 두 개 이상의 레코드(동일한 카탈로그 파일 또는 다른 카탈로그 파일)에서 발생하고 마지막 인스턴스가 우세합니다.

## 속성 {#section-6da55f145ecd4e31a5de52637a436983}

쉼표로 구분된 하나 이상의 텍스트 문자열 값. 선택적. 각 값은 카탈로그 폴더에 상대적인 절대 파일 경로 또는 경로여야 합니다.

## 기본값 {#section-80f91cd7a6b2479ebb310319e9c74da7}

비어 있음 - 이 이미지 카탈로그에 이미지 데이터가 포함되어 있지 않음을 나타냅니다.

## 참조 {#section-910b67c5041d44d99a105ad43ff63a37}

[카탈로그 데이터 필드](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
