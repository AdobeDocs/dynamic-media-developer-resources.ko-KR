---
description: 이미지 파일 경로입니다.
solution: Experience Manager
title: 경로
topic: Scene7 Image Serving - Image Rendering API
uuid: 0fca88bb-de00-4eff-83ad-c0f5e3b8ece0
translation-type: tm+mt
source-git-commit: 7b837020deef888a038a074d0aa826d43e60aeb6
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 4%

---


# 경로{#path}

이미지 파일 경로입니다.

이 카탈로그 레코드와 연관된 소스 이미지 파일의 상대 또는 절대 경로와 이름입니다. 서버는 소스 데이터 관리에 설명된 경로 해결 규칙을 사용하여 데이터 파일을 찾습니다.

## 속성 {#path-properties}

텍스트 문자열. 이미지 레코드에 필요한 경우 템플릿 레코드에 대해 비어 있을 수 있습니다. 지정된 경우 올바른 상대 또는 절대 이미지 서버 파일 경로여야 합니다. 속성::DefaultExt는 파일 접미사가 없는 경우 추가됩니다.

## 지원되는 이미지 파일 형식 {#path-supported-image-file-formats}

지원되는 파일 형식의 전체 목록은 IC(Image Converter) 유틸리티의 설명을 참조하십시오.

여러 해상도의 이미지 데이터가 필요한 응용 프로그램은 Dynamic Media PTIFF(Pyramid TIFF) 다중 해상도 형식을 사용할 때 가장 잘 수행됩니다. IC 유틸리티는 지원되는 모든 이미지 포맷에서 PTIFF 이미지를 만드는 데 사용됩니다.

## 기본값 {#path-default}

없음.

## 참조 {#path-seealso}

[IC 유틸리티](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) ,  [속성::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) ,  [속성::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md) ,  [src=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md)

<!-- [attribute::LowerCasePaths]() -->