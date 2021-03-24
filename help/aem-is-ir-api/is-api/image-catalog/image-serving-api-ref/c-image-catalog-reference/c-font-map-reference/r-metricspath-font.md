---
description: 글꼴 지표 파일 경로. 파일 접미사를 포함한 글꼴 지표 파일의 경로 및 이름입니다.
solution: Experience Manager
title: 지표 경로
feature: Dynamic Media Classic,SDK/API
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 4%

---


# MetricsPath{#metricspath}

글꼴 지표 파일 경로. 파일 접미사를 포함한 글꼴 지표 파일의 경로 및 이름입니다.

Adobe Type 1 글꼴에 사용됩니다. 지정하지 않으면 서버가 주글꼴 파일이 있는 동일한 폴더에서 글꼴 지표 파일을 찾으려고 시도합니다. 렌더링할 때 필요한 글꼴 지표 파일을 찾을 수 없는 경우 오류가 발생합니다.

## 속성 {#section-955268c581574875b05253d9e14544f3}

텍스트 문자열. Adobe Type 1 파일(선택 사항) 비어 있거나 유효한 이미지 서버 파일 경로여야 합니다(절대 경로이거나 `attribute::RootPath`에 상대적입니다.

## 기본값 {#section-a6ffbd6879c642caa5a2fd4ed14a3a85}

없음.

## 참조 {#section-a3a87a03d8e14876b7dbc2d4ad45c5ef}

[특성::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md)
