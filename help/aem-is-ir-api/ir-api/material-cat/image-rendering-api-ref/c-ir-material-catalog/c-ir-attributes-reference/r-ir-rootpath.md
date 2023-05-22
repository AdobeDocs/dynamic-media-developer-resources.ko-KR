---
title: 루트 경로
description: 소스 데이터 루트 경로. 텍스트 문자열 값입니다. 이 이미지 카탈로그에서 참조한 모든 비네팅, 텍스처, 이미지 및 ICC 데이터 파일의 루트 폴더에 대한 절대 경로 또는 상대 경로 세그먼트입니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0eecb125-8147-4115-883a-cb6c38333270
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 2%

---

# 루트 경로{#rootpath}

소스 데이터 루트 경로. 텍스트 문자열 값입니다. 이 이미지 카탈로그에서 참조한 모든 비네팅, 텍스처, 이미지 및 ICC 데이터 파일의 루트 폴더에 대한 절대 경로 또는 상대 경로 세그먼트입니다.

## 속성 {#section-5ff1cf592dd24dfc8cfa470c753ab828}

텍스트 문자열입니다. 이미지 렌더링 서버 구성 설정에 상대적인 유효한 경로 세그먼트가 비어 있어야 합니다. `ir.resourceRootPaths`또는 유효한 절대 파일 경로입니다. 선행 및 후행 경로 요소 구분 기호를 포함해서는 안 됩니다.

## 기본값 {#section-4a7f3ab22b0c4090b3896d29bd192b8a}

상속 위치 `default::RootPath` 정의되지 않은 경우. 정의되어 있지만 비어 있는 경우 소스 파일 루트 경로에 기여하지 않습니다.

## 참조 {#section-92012cc1ce32448ea977e7e0484857e2}

[catalog::Path](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-path.md#reference-59ebb624250a4965ad1737578a2ab590) , [catalog::AuxPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-auxpath.md#reference-943ad5ee3c3b4b06bbcbb005db0dc969), `ir.resourceRootPaths`
