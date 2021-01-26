---
description: 카탈로그 레코드 식별자
solution: Experience Manager
title: ID
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 9803d754-1f94-4e5d-9a40-3936676c0035
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 8%

---


# ID {#id}

Platform Server에서 이미지 데이터 파일의 레코드를 조회하는 인덱스 키 값입니다.

일반적으로 SKU에 이미지가 여러 개인 경우 SKU 번호와 같은 짧고 고유한 이미지 ID입니다. 이미지 제공 기능을 사용하여 웹 사이트를 손쉽게 복고적으로 맞출 수 있도록 파일 경로와 유사하게 보이는 보다 복잡한 문자열일 수도 있습니다.

## 속성 {#id-properties}

텍스트 문자열. 필수. 이미지 데이터 테이블에 대한 기본 인덱스 키입니다. 각 카탈로그::Id 값은 테이블 내에서 고유해야 합니다.

## 기본값 {#id-default}

없음.

## 참조 {#id-seealso}

[특성::RootId](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md)