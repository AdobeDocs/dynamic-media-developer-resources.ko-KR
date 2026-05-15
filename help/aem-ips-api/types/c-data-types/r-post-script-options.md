---
description: PostScript 파일 옵션입니다.
solution: Experience Manager
title: PostScript 옵션
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fd2093b5-9856-4f31-8853-1027194a71df
TQID: 'https://experienceleague.adobe.com/XsIiYor0c-7I34OYazNaSF0Hx3sbZmzpTzAT1u73xxo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 65
ht-degree: 12%

---

# [!DNL PostScriptOptions]{#postscriptoptions}

PostScript 파일 옵션입니다.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| 프로세스 | `xsd:string` | PostScript 프로세스 선택. |
| 해상도 | `xsd:double` | 파일 확인. |
| 색상 공간 | `xsd:string` | PostScript 색상 공간 모드. |
| 알파 | `xsd:boolean` | 파일을 이미지로 래스터화할지 여부입니다. 원본 파일 가 이러한 방식으로 정의된 경우 투명 배경이 만들어집니다. 일반적으로 오버레이 로고를 만드는 데 사용됩니다. |
| extractSearchwords | `xsd:boolean` | PostScript 파일에서 검색어를 추출할지 여부입니다. |
