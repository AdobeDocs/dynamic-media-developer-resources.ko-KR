---
description: PDF 파일에서 추출한 문자열 레코드를 검색합니다.
seo-description: PDF 파일에서 추출한 문자열 레코드를 검색합니다.
seo-title: SearchStrings
solution: Experience Manager
title: SearchStrings
topic: Scene7 Image Production System API
uuid: aade2741-3e77-44c6-ab3c-0810ff034412
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SearchStrings{#searchstrings}

PDF 파일에서 추출한 문자열 레코드를 검색합니다.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| ` *`searchString`*` | `xsd:string` | 문자열 텍스트를 검색합니다. |
| ` *`keywordsArray`*` | `types:KeywordsArray` | 검색 문자열에서 키워드의 배열입니다. |
| ` *`status`*` | `xsd:boolean` | 검색 문자열이 유효하고 활성화되어 있으면 true입니다. |
| ` *`x`*` | `xsd:int` | 검색 문자열의 X축 위치입니다. |
| ` *`y`*` | `xsd:int` | 검색 문자열의 Y축 위치입니다. |
| ` *`width`*` | `xsd:int` | 문자열 너비를 검색합니다. |
| ` *`height`*` | `xsd:int` | 문자열 높이를 검색합니다. |
| ` *`fontName`*` | `xsd:string` | 검색 문자열에서 사용되는 글꼴의 이름입니다. |
| ` *`pointSize`*` | `xsd:string` | 글꼴 크기. |

