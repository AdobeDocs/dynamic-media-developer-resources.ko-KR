---
description: 카탈로그 레코드 식별자
solution: Experience Manager
title: Id
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 37945115-c93d-4f59-b3d3-a2c4ee7fc990
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 5%

---

# Id {#id}

이미지 데이터 파일에서 레코드를 조회하는 인덱스 키 값 [!DNL Platform Server].

일반적으로 SKU에 여러 이미지가 있는 경우 일종의 이미지 접미사가 있을 수 있는 SKU 번호와 같은 짧고 고유한 이미지 식별자입니다. 이미지 제공으로 웹 사이트의 쉬운 리트로 피팅을 지원하기 위해 파일 경로처럼 보이는 보다 복잡한 문자열일 수도 있습니다.

## 속성 {#id-properties}

텍스트 문자열입니다. 필수. 이미지 데이터 테이블에 대한 기본 인덱스 키입니다. 각 카탈로그::Id 값은 테이블 내에서 고유해야 합니다.

## 기본값 {#id-default}

없음.

## 참조 {#id-seealso}

[attribute::RootId](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md)
