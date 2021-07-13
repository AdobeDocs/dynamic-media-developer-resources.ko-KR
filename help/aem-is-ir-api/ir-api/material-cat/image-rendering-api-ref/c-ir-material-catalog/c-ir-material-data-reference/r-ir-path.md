---
description: 이미지 파일 경로입니다. 텍스처 또는 decal 이미지 파일의 상대 경로 및 이름입니다.
solution: Experience Manager
title: 경로 *
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 28758709-26ae-4261-b11e-34e37b9d1b8c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 3%

---

# 경로 *{#path}

이미지 파일 경로입니다. 텍스처 또는 decal 이미지 파일의 상대 경로 및 이름입니다.

서버는 이 값을 `attribute::RootPath`과 결합하여 실제 이미지 파일 경로를 만듭니다. 절대 경로일 수도 있습니다.

텍스처, 캐비닛 및 창 커버 재료의 텍스처 이미지 파일과 십진수 및 벽 테두리 재료용 RGB 또는 RGBA 이미지 파일을 지정하는 데 사용됩니다. 모든 캐비닛 및 창 커버 재료는 별도의 반복 가능한 텍스쳐 이미지가 필요한 것은 아닙니다.

## 속성 {#section-8c12ea24f21d4472be677581893e6681}

텍스트 문자열입니다. 텍스쳐 및 디칼 재질에 필요한 캐비닛 및 윈도우 커버 재질의 옵션 지정하면 유효한 상대 또는 절대 파일 경로여야 합니다. 단색 재료의 경우 비어 있어야 합니다.

## 지원되는 파일 형식 {#section-7ef6c9f7c72c4f03ae926d030b6c46d8}

이미지 렌더링은 Dynamic Media 이미지 제공 기능과 동일한 소스 이미지 형식을 지원합니다.

여러 해상도의 이미지 데이터가 필요한 응용 프로그램은 Dynamic Media 피라미드 TIFF(PTIFF) 다중 해상도 형식을 사용할 때 가장 잘 수행됩니다. 이미지 제공 기능에는 지원되는 모든 포맷에서 PTIFF 이미지를 생성하는 IC(Image Converter) 유틸리티가 포함되어 있습니다.

지원되는 파일 형식의 전체 목록은 이미지 제공 설명서의 IC 유틸리티에 대한 설명을 참조하십시오.

## 기본값 {#section-d2e91fcd7d3c45edb34e7d5ae1daadda}

없음.

## 참조 {#section-1bf37fab8e5f4c42a03b785abafc53bd}

[IC 유틸리티](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) ,  [속성::RootPath](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md),  [src=](/help/aem-is-ir-api/ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md)
