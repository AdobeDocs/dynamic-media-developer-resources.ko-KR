---
description: PDF 파일 옵션입니다.
solution: Experience Manager
title: PDF 옵션
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 140c9261-e590-4889-9be4-29afd19ffa86
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 10%

---

# [!DNL PDFOptions]{#pdfoptions}

PDF 파일 옵션입니다.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| 프로세스 | `xsd:string` | &quot;PDF 프로세스&quot; 선택 |
| 해상도 | `xsd:double` | 파일 확인. |
| 색상 공간 | `xsd:string` | 사후 스크립트 색상 공간 모드 선택. |
| pdfCatalog | `xsd:boolean` | 렌더링 후 여러 페이지 PDF을 eCatalog에 결합할지 여부입니다(기본값은 true). |
| extractSearchwords | `xsd:boolean` | PDF 파일에서 검색어를 추출할지 여부입니다. |
| extractLink | `xsd:boolean` | IPS 내의 래스터화된 페이지에 지정된 이미지 맵에 PDF 링크를 추출할지 여부입니다. |
