---
description: 글꼴 지표 파일 경로입니다. 파일 접미사를 포함하여 글꼴 지표 파일의 경로 및 이름입니다.
solution: Experience Manager
title: 지표 경로
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0f1f98a5-b53b-4e20-b4c8-e70482b01a04
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 4%

---

# 지표 경로{#metricspath}

글꼴 지표 파일 경로입니다. 파일 접미사를 포함하여 글꼴 지표 파일의 경로 및 이름입니다.

Adobe Type 1 글꼴에 사용됩니다. 지정하지 않으면 서버가 주 글꼴 파일이 있는 동일한 폴더에서 글꼴 지표 파일을 찾습니다. 렌더링 시 필요한 글꼴 지표 파일을 찾을 수 없으면 오류가 발생합니다.

## 속성 {#section-955268c581574875b05253d9e14544f3}

텍스트 문자열입니다. Adobe Type 1 파일에 선택 사항입니다. 비어 있거나 유효한 이미지 서버 파일 경로여야 합니다(절대 또는 `attribute::RootPath` 상대).

## 기본값 {#section-a6ffbd6879c642caa5a2fd4ed14a3a85}

없음.

## 참조 {#section-a3a87a03d8e14876b7dbc2d4ad45c5ef}

[attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md)
