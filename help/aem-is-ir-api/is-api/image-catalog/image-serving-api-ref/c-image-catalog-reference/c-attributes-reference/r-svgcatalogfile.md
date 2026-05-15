---
description: SVG 데이터 파일 경로. 이 카탈로그의 SVG 데이터가 포함된 파일을 지정합니다.
solution: Experience Manager
title: SvgCatalogFile
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 654579a2-33ff-4633-a6d0-3c03ec8d5aed
TQID: 'https://experienceleague.adobe.com/m1-nKj-KiVQlN70GYy1AFAAQN-M1wnxTGmmj-e3t9AY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 115
ht-degree: 3%

---

# SvgCatalogFile{#svgcatalogfile}

SVG 데이터 파일 경로. 이 카탈로그의 SVG 데이터가 포함된 파일을 지정합니다.

SVG 데이터 파일은 지정된 정확한 순서로 모든 이미지 데이터 파일 뒤에 로드됩니다. 동일한 `catalog::Id` 값이 둘 이상의 레코드(같거나 다른 이미지 또는 SVG 카탈로그 파일)에 있으면 마지막 인스턴스가 우세합니다.

## 속성 {#section-fc2d549f76474792837b2b92ec2087ea}

쉼표로 구분된 하나 이상의 텍스트 문자열 값. 선택적. 각 값은 카탈로그 폴더에 상대적인 절대 파일 경로 또는 경로여야 합니다.

## 기본값 {#section-a4e58951f3c249599665b823566433c9}

비어 있음 - 이 이미지 카탈로그에 SVG 데이터가 포함되지 않았음을 나타냅니다.

## 참조 {#section-dad6cf4cc5994cf5bbed8807c96119dd}

[카탈로그 데이터](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29), [카탈로그 파일](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-catalogfile.md#reference-16498bb4cb33458697c1ab002ea8db79)
