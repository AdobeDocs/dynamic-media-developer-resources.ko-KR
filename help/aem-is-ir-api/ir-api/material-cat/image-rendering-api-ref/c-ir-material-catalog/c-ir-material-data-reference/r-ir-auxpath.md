---
description: 데이터 파일 경로. 이 이미지와 연결된 이미지가 아닌 데이터 파일의 상대 경로 및 이름입니다.
solution: Experience Manager
title: 보조 경로
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 55f82596-72f0-48c4-9b3a-f10ea5f610f1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 3%

---

# 보조 경로{#auxpath}

데이터 파일 경로. 이 이미지와 연결된 이미지가 아닌 데이터 파일의 상대 경로 및 이름입니다.

서버는 이 값을 attribute::RootPath와 결합하여 실제 파일 경로를 작성합니다. 절대 파일 경로일 수도 있습니다.

캐비닛 재료에 대한 캐비닛 스타일 파일 또는 창 커버 재료에 대한 창 커버 스타일 파일을 지정하는 데 사용됩니다. 다른 모든 자료는 비워 두십시오.

## 속성 {#section-4268350054b7421da0ce0327f0731a52}

텍스트 문자열 값입니다. 지정하면 유효한 상대 또는 절대 파일 경로여야 합니다. 캐비닛 재료 및 창 덮개 재료에 필요합니다. 다른 모든 자료는 비어 있어야 합니다.

## 기본값 {#section-287005c2d8e948fa958f69ba7b90b437}

없음.

## 참조 {#section-e1f7a61c00d04a80af28e2e67481ab92}

[특성::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3) , [카탈로그::Path](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-path.md#reference-59ebb624250a4965ad1737578a2ab590), [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
