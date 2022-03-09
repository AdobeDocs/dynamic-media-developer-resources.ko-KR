---
description: 자산 또는 폴더의 디스크 공간 통계입니다.
solution: Experience Manager
title: DiskUsage
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: a3c4c1cd-0fcc-4e7a-a4aa-884d0ce2f208
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '51'
ht-degree: 13%

---

# DiskUsage{#diskusage}

자산 또는 폴더의 디스크 공간 통계입니다.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| companyHandle | `xsd:string` | 회사 핸들. |
| companyName | `xsd:string` | 회사 이름. |
| imageCount | `xsd:int` | 저장된 이미지 수. |
| diskSpaceUsage | `xsd:long` | 총 파일 측면(KB)입니다. |
| lastModified | `xsd:dateTime` | 날짜, 시간 및 시간대 `DiskUsage` 유형이 마지막으로 수정되었습니다. |
