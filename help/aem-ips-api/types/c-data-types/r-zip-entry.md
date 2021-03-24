---
description: ZIP 파일의 항목입니다.
solution: Experience Manager
title: ZipEntry
feature: Dynamic Media Classic,SDK/API
role: 개발자,관리자
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '50'
ht-degree: 12%

---


# ZipEntry{#zipentry}

ZIP 파일의 항목입니다.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| `*`name`*` | `xsd:string` | 응모 이름. |
| `*`isDirectory`*` | `xsd:boolean` | 항목이 디렉토리인지 확인합니다. |
| `*`lastModified`*` | `xsd:dateTime` | 마지막 수정 날짜 및 시간입니다. |
| `*`compressedSize`*` | `xsd:long` | 압축된 크기. |
| `*`uncompressedSize`*` | `xsd:long` | 압축되지 않은 크기입니다. |

