---
description: 자산 또는 폴더에 대한 디스크 공간 통계입니다.
seo-description: 자산 또는 폴더에 대한 디스크 공간 통계입니다.
seo-title: DiskUsage
solution: Experience Manager
title: DiskUsage
topic: Scene7 Image Production System API
uuid: a63f0ed0-c689-43b0-9c3e-9500715d15a5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# DiskUsage{#diskusage}

자산 또는 폴더에 대한 디스크 공간 통계입니다.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 회사 핸들 |
| ` *`companyName`*` | `xsd:string` | 회사 이름. |
| ` *`imageCount`*` | `xsd:int` | 저장된 이미지 수입니다. |
| ` *`diskSpaceUsage`*` | `xsd:long` | 총 파일 측면(KB)입니다. |
| ` *`lastModified`*` | `xsd:dateTime` | 유형이 마지막으로 수정된 날짜, 시간 및 `DiskUsage` 표준 시간대 |

