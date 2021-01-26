---
description: 주 작업 로그 메시지(JobDetail)와 연결된 보조 메시지를 포함합니다. 현재 처리된 자산과 관련된 경고 및 기타 세부 사항을 포함합니다.
seo-description: 주 작업 로그 메시지(JobDetail)와 연결된 보조 메시지를 포함합니다. 현재 처리된 자산과 관련된 경고 및 기타 세부 사항을 포함합니다.
seo-title: JobLogDetailAux
solution: Experience Manager
title: JobLogDetailAux
topic: Dynamic Media Image Production System API
uuid: df6f61f2-54f1-4996-938c-c3ea8c27551a
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 5%

---


# JobLogDetailAux{#joblogdetailaux}

주 작업 로그 메시지(JobDetail)와 연결된 보조 메시지를 포함합니다. 현재 처리된 자산과 관련된 경고 및 기타 세부 사항을 포함합니다.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| `*`logMessage`*` | `xsd:string` | 보조 메시지입니다. |
| `*`logType`*` | `xsd:string` | 로그 유형:`IPSJobLog.gcUploadWarning` 또는 `IPSJobLog.gcUploadError`. |
| `*`dateCreated`*` | `xsd:dateTime` | 보조 작업 로그 생성 날짜입니다. |

