---
description: 이미지 파일 경로.
solution: Experience Manager
title: 경로
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9d5417df-3aa2-4620-a614-ca71a96e2069
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 4%

---

# 경로{#path}

이미지 파일 경로.

이 카탈로그 레코드와 연결된 소스 이미지 파일의 상대 또는 절대 경로 및 이름입니다. 서버는 소스 데이터 관리에 설명된 경로 확인 규칙을 사용하여 데이터 파일을 찾습니다.

## 속성 {#path-properties}

텍스트 문자열입니다. 이미지 레코드에 필요합니다. 템플릿 레코드에 대해 비어 있을 수 있습니다. 지정하면 올바른 상대 또는 절대 이미지 서버 파일 경로여야 합니다. 파일 접미사가 없으면 attribute::DefaultExt가 추가됩니다.

## 지원되는 이미지 파일 형식 {#path-supported-image-file-formats}

지원되는 파일 형식의 전체 목록은 이미지 변환기(IC) 유틸리티의 설명을 참조하십시오.

여러 다른 해상도의 이미지 데이터가 필요한 응용 프로그램은 Dynamic Media 피라미드 TIFF(PTIFF) 다중 해상도 형식을 사용할 때 가장 잘 수행됩니다. IC 유틸리티는 지원되는 모든 이미지 형식에서 PTIFF 이미지를 생성하는 데 사용됩니다.

## 기본값 {#path-default}

없음.

## 참조 {#path-seealso}

[IC 유틸리티](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) , [attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) , [attribute::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md) , [src=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md)

<!-- [attribute::LowerCasePaths]() -->
