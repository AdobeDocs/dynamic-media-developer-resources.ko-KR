---
description: ZIP 파일의 항목입니다.
solution: Experience Manager
title: ZipEntry
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: f71f57db-6717-4a27-b275-19bc4cf59ea4
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 12%

---

# ZipEntry{#zipentry}

ZIP 파일의 항목입니다.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| `*`name`*` | `xsd:string` | 항목 이름. |
| `*`isDirectory`*` | `xsd:boolean` | 항목이 디렉터리인지 확인합니다. |
| `*`lastModified`*` | `xsd:dateTime` | 마지막 수정 날짜 및 시간입니다. |
| `*`compressedSize`*` | `xsd:long` | 압축 크기입니다. |
| `*`uncompressedSize`*` | `xsd:long` | 압축되지 않은 크기입니다. |
