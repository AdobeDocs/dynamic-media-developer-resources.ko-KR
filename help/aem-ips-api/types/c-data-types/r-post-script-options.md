---
description: PostScript 파일 옵션.
solution: Experience Manager
title: PostScriptOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fd2093b5-9856-4f31-8853-1027194a71df
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 11%

---

# PostScriptOptions{#postscriptoptions}

PostScript 파일 옵션.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| `*`프로세스`*` | `xsd:string` | PostScript 프로세스 선택. |
| `*`resolution`*` | `xsd:double` | 파일 해상도. |
| `*`색상 공간`*` | `xsd:string` | PostScript colorspace 모드. |
| `*`alpha`*` | `xsd:boolean` | 파일을 이미지로 래스터화할지 여부. 원본 파일이 이러한 방식으로 정의된 경우 투명 배경을 만듭니다. 일반적으로 오버레이 로고를 만드는 데 사용됩니다. |
| `*`extractSearchWords`*` | `xsd:boolean` | PostScript 파일에서 검색어를 추출할지 여부. |
