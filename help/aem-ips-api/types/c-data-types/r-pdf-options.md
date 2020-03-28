---
description: PDF 파일 옵션
seo-description: PDF 파일 옵션
seo-title: PDFptions
solution: Experience Manager
title: PDFptions
topic: Scene7 Image Production System API
uuid: 7558b6b5-ad32-4baf-896b-f4e2bd48f2ec
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# PDFptions{#pdfoptions}

PDF 파일 옵션

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| ` *`프로세스`*` | `xsd:string` | &quot;PDF 프로세스&quot;의 선택 |
| ` *`resolution`*` | `xsd:double` | 파일 해상도. |
| ` *`색상 공간`*` | `xsd:string` | 사후 스크립트 색상 공간 모드 선택 |
| ` *`pdfCatalog`*` | `xsd:boolean` | 렌더링 후 여러 페이지 PDF를 eCatalog로 결합할지 여부(기본값: true). |
| ` *`extractSearchWords`*` | `xsd:boolean` | PDF 파일에서 검색어를 추출할지 여부 |
| ` *`extractLinks`*` | `xsd:boolean` | IPS 내에서 래스터화된 페이지에 할당된 이미지 맵에 PDF 링크를 추출할지 여부 |

