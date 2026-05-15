---
description: PDF 파일 옵션입니다.
solution: Experience Manager
title: PDF 옵션
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 140c9261-e590-4889-9be4-29afd19ffa86
TQID: 'https://experienceleague.adobe.com/gjd-g7jhWVbLRL3kYnkX96ihjkiK34oCp7Ns1iC89GM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 68
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
