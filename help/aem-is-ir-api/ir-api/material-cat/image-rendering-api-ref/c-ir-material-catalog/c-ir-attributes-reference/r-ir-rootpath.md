---
description: 소스 데이터 루트 경로. 텍스트 문자열 값입니다. 이 이미지 카탈로그에서 참조하는 모든 비네팅, 텍스처, 이미지 및 ICC 데이터 파일에 대한 루트 폴더의 절대 경로 또는 상대 경로 세그먼트입니다.
solution: Experience Manager
title: 루트 경로 *
feature: Dynamic Media Classic,SDK/API
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 3%

---


# 루트 경로 *{#rootpath}

소스 데이터 루트 경로. 텍스트 문자열 값입니다. 이 이미지 카탈로그에서 참조하는 모든 비네팅, 텍스처, 이미지 및 ICC 데이터 파일에 대한 루트 폴더의 절대 경로 또는 상대 경로 세그먼트입니다.

## 속성 {#section-5ff1cf592dd24dfc8cfa470c753ab828}

텍스트 문자열. 비어 있거나, 이미지 렌더링 서버 구성 설정 `ir.resourceRootPaths`에 상대적인 유효한 경로 세그먼트 또는 유효한 절대 파일 경로여야 합니다. 행간 및 후행 패스 요소 구분 기호는 포함할 수 없습니다.

## 기본값 {#section-4a7f3ab22b0c4090b3896d29bd192b8a}

정의되지 않은 경우 `default::RootPath`에서 상속됩니다. 정의되어 있지만 비어 있으면 소스 파일 루트 경로에 기여하지 않습니다.

## 참조 {#section-92012cc1ce32448ea977e7e0484857e2}

[카탈로그::경로](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-path.md#reference-59ebb624250a4965ad1737578a2ab590) ,  [카탈로그::AuxPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-auxpath.md#reference-943ad5ee3c3b4b06bbcbb005db0dc969),  `ir.resourceRootPaths`
