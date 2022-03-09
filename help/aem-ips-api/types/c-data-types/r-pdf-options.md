---
description: PDF 파일 옵션.
solution: Experience Manager
title: PDFOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 140c9261-e590-4889-9be4-29afd19ffa86
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 11%

---

# PDFOptions{#pdfoptions}

PDF 파일 옵션.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| 프로세스 | `xsd:string` | PDF 프로세스 선택 |
| 해상도 | `xsd:double` | 파일 해상도. |
| 색상 공간 | `xsd:string` | 사후 스크립트 Colorspace 모드 선택. |
| pdfCatalog | `xsd:boolean` | 렌더링 후 여러 페이지 PDF을 eCatalog에 결합할지 여부(기본값은 true). |
| extractSearchWords | `xsd:boolean` | PDF 파일에서 검색어를 추출할지 여부. |
| extractLinks | `xsd:boolean` | IPS 내에서 래스터화된 페이지에 할당된 이미지 맵에 PDF 링크를 추출할지 여부. |
