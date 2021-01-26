---
description: 작업 항목 진행 정보.
seo-description: 작업 항목 진행 정보.
seo-title: 작업 항목 진행
solution: Experience Manager
title: 작업 항목 진행
topic: Dynamic Media Image Production System API
uuid: 7cca2ad9-c8f9-4dff-a055-d03fa2c50cec
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '38'
ht-degree: 15%

---


# TaskItemProgress{#taskitemprogress}

작업 항목 진행 정보.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| `*`itemName`*` | `xsd:string` | 처리 중인 항목의 이름입니다. |
| `*`progress`*` | `xsd:double` | 진행 완료 %. |
| `*`progressMessage`*` | `xsd:string` | 프로세스 메시지. |
| `*`lastProgressUpdate`*` | `xsd:dateTime` | 마지막 업데이트 시간입니다. |

