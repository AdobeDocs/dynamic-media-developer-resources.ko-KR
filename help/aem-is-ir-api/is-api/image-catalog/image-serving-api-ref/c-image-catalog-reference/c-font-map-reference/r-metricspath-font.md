---
description: 글꼴 지표 파일 경로입니다. 파일 접미사를 포함한 글꼴 지표 파일의 경로 및 이름입니다.
solution: Experience Manager
title: 지표 경로
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0f1f98a5-b53b-4e20-b4c8-e70482b01a04
TQID: 'https://experienceleague.adobe.com/XPXcnrT94IfPupctNoxqN7-qYCuxdeoqXQeBkM1Un4k'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 107
ht-degree: 3%

---

# 지표 경로{#metricspath}

글꼴 지표 파일 경로입니다. 파일 접미사를 포함한 글꼴 지표 파일의 경로 및 이름입니다.

Adobe Type 1 글꼴에 사용됩니다. 지정하지 않으면 서버는 기본 글꼴 파일이 있는 동일한 폴더에서 글꼴 지표 파일을 찾으려고 합니다. 렌더링 시 필요한 글꼴 지표 파일을 찾을 수 없는 경우 오류가 발생합니다.

## 속성 {#section-955268c581574875b05253d9e14544f3}

텍스트 문자열입니다. Adobe Type 1 파일의 경우 선택 사항입니다. 비어 있거나 `attribute::RootPath`에 대한 절대 또는 상대 이미지 서버 파일 경로가 유효해야 합니다.

## 기본값 {#section-a6ffbd6879c642caa5a2fd4ed14a3a85}

없음.

## 참조 {#section-a3a87a03d8e14876b7dbc2d4ad45c5ef}

[attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md)
