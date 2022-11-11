---
description: ZIP 파일의 항목입니다.
solution: Experience Manager
title: ZipEntry
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f71f57db-6717-4a27-b275-19bc4cf59ea4
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '42'
ht-degree: 14%

---

# [!DNL ZipEntry]{#zipentry}

ZIP 파일의 항목입니다.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| 이름 | `xsd:string` | 항목 이름. |
| isDirectory | `xsd:boolean` | 항목이 디렉터리인지 확인합니다. |
| lastModified | `xsd:dateTime` | 마지막 수정 날짜 및 시간입니다. |
| compressedSize | `xsd:long` | 압축 크기입니다. |
| uncompressedSize | `xsd:long` | 압축되지 않은 크기입니다. |
