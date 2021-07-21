---
description: PDF 파일에서 추출한 검색 문자열 레코드입니다.
solution: Experience Manager
title: SearchStrings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 3f67ba8a-12dd-4698-9502-7cbdec9cb25d
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 11%

---

# SearchStrings{#searchstrings}

PDF 파일에서 추출한 검색 문자열 레코드입니다.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| `*`searchString`*` | `xsd:string` | 문자열 텍스트를 검색합니다. |
| `*`keywordsArray`*` | `types:KeywordsArray` | 검색 문자열에서 키워드 배열입니다. |
| `*`status`*` | `xsd:boolean` | 검색 문자열이 유효하고 활성화되어 있으면 True입니다. |
| `*`x`*` | `xsd:int` | 검색 문자열의 X축 위치입니다. |
| `*`y`*` | `xsd:int` | 검색 문자열의 Y축 위치입니다. |
| `*`width`*` | `xsd:int` | 검색 문자열 너비. |
| `*`height`*` | `xsd:int` | 검색 문자열 높이. |
| `*`fontName`*` | `xsd:string` | 검색 문자열에 사용되는 글꼴의 이름입니다. |
| `*`pointSize`*` | `xsd:string` | 글꼴 크기입니다. |
