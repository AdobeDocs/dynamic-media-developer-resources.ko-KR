---
description: PDF 파일에서 추출된 검색 문자열 레코드입니다.
solution: Experience Manager
title: 검색 문자열
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 3f67ba8a-12dd-4698-9502-7cbdec9cb25d
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 12%

---

# [!DNL SearchStrings]{#searchstrings}

PDF 파일에서 추출된 검색 문자열 레코드입니다.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| searchString | `xsd:string` | 검색 문자열 텍스트입니다. |
| keywordsArray | `types:KeywordsArray` | 검색 문자열의 키워드 배열. |
| status | `xsd:boolean` | 검색 문자열이 유효하고 활성화되면 True입니다. |
| x | `xsd:int` | 검색 문자열의 X축 위치입니다. |
| y | `xsd:int` | 검색 문자열의 Y축 위치입니다. |
| 너비 | `xsd:int` | 검색 문자열 너비입니다. |
| 높이 | `xsd:int` | 검색 문자열 높이입니다. |
| fontName | `xsd:string` | 검색 문자열에 사용되는 글꼴의 이름입니다. |
| pointSize | `xsd:string` | 글꼴 크기입니다. |
