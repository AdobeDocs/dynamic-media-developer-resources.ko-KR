---
description: PDF 파일 옵션.
solution: Experience Manager
title: PDFOptions
feature: Dynamic Media Classic,SDK/API
role: 개발자,관리자
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 9%

---


# PDFOptions{#pdfoptions}

PDF 파일 옵션.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| `*`프로세스`*` | `xsd:string` | &quot;PDF 프로세스&quot;를 선택합니다. |
| `*`resolution`*` | `xsd:double` | 파일 해상도. |
| `*`색상 공간`*` | `xsd:string` | [사후 스크립트 색상 공간 모드]를 선택합니다. |
| `*`pdfCatalog`*` | `xsd:boolean` | 렌더링 후 여러 페이지 PDF를 eCatalog로 결합할지 여부(기본값: true). |
| `*`extractSearchWords`*` | `xsd:boolean` | PDF 파일에서 검색어를 추출할지 여부. |
| `*`extractLinks`*` | `xsd:boolean` | IPS 내의 래스터화된 페이지에 할당된 이미지 맵에 PDF 링크를 추출할지 여부. |

