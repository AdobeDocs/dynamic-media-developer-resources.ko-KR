---
description: ZIP 파일의 항목.
solution: Experience Manager
title: 우편번호 입력
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f71f57db-6717-4a27-b275-19bc4cf59ea4
TQID: 'https://experienceleague.adobe.com/u8w7i9pPiCJTkbxwQXg-IBIz3hDWtxrEvqNJ5JERM64'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 42
ht-degree: 14%

---

# [!DNL ZipEntry]{#zipentry}

ZIP 파일의 항목.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| name | `xsd:string` | 항목 이름. |
| isDirectory | `xsd:boolean` | 항목이 디렉터리인지 확인합니다. |
| 마지막 수정일 | `xsd:dateTime` | 마지막 수정 날짜 및 시간입니다. |
| compressedSize | `xsd:long` | 압축 크기. |
| uncompressedSize | `xsd:long` | 압축되지 않은 크기입니다. |
