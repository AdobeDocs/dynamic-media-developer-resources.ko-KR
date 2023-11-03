---
description: 이미지 파일 경로. 텍스처 또는 데칼 이미지 파일의 상대 경로 및 이름입니다.
solution: Experience Manager
title: 경로 *
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 28758709-26ae-4261-b11e-34e37b9d1b8c
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 2%

---

# 경로 *{#path}

이미지 파일 경로. 텍스처 또는 데칼 이미지 파일의 상대 경로 및 이름입니다.

서버는 이 값을 와 결합합니다 `attribute::RootPath` 실제 이미지 파일 경로를 빌드합니다. 절대 경로일 수도 있습니다.

텍스처, 캐비닛 및 창 커버링 재료에 대한 텍스처 이미지 파일과 데칼 및 벽 테두리 재료에 대한 RGB 또는 RGBA 이미지 파일을 지정하는 데 사용됩니다. 모든 캐비닛 및 창 커버링 재료가 별도의 반복 가능한 텍스처 이미지를 필요로 하는 것은 아닙니다.

## 속성 {#section-8c12ea24f21d4472be677581893e6681}

텍스트 문자열입니다. 텍스처 및 데칼 소재에 필요하며, 캐비닛 및 창 덮개 소재에 선택 사항입니다. 지정하면 유효한 상대 또는 절대 파일 경로여야 합니다. 단색 소재의 경우 비어 있어야 합니다.

## 지원되는 파일 형식 {#section-7ef6c9f7c72c4f03ae926d030b6c46d8}

이미지 렌더링은 Dynamic Media 이미지 제공과 동일한 소스 이미지 형식을 지원합니다.

서로 다른 여러 해상도의 이미지 데이터가 필요한 응용 프로그램은 Dynamic Media 피라미드 TIFF(PTIFF) 다중 해상도 형식을 사용할 때 가장 잘 수행됩니다. 이미지 제공에는 지원되는 모든 형식에서 PTIFF 이미지를 생성하는 이미지 변환기(IC) 유틸리티가 포함되어 있습니다.

지원되는 파일 형식의 전체 목록은 이미지 제공 설명서의 IC 유틸리티 설명을 참조하십시오.

## 기본값 {#section-d2e91fcd7d3c45edb34e7d5ae1daadda}

없음.

## 참조 {#section-1bf37fab8e5f4c42a03b785abafc53bd}

[IC 유틸리티](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) , [attribute::RootPath](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md), [src=](/help/aem-is-ir-api/ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md)
