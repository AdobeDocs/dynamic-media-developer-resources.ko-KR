---
description: 자산 또는 폴더에 대한 디스크 공간 통계.
solution: Experience Manager
title: 디스크 사용량
feature: Dynamic Media Classic,SDK/API
role: 개발자,관리자
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 12%

---


# DiskUsage{#diskusage}

자산 또는 폴더에 대한 디스크 공간 통계.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 회사 핸들. |
| `*`companyName`*` | `xsd:string` | 회사 이름. |
| `*`imageCount`*` | `xsd:int` | 저장된 이미지 수입니다. |
| `*`diskSpaceUsage`*` | `xsd:long` | 전체 파일 측면(KB)입니다. |
| `*`lastModified`*` | `xsd:dateTime` | `DiskUsage` 유형의 날짜, 시간 및 시간대가 마지막으로 수정되었습니다. |

