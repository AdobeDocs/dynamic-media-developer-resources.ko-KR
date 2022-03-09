---
description: 주 작업 로그 메시지와 관련된 보조 메시지(JobDetail)를 포함합니다. 현재 처리된 자산과 관련된 경고 및 기타 세부 정보를 포함합니다.
solution: Experience Manager
title: 작업 로그 세부 정보
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 789736c5-d74d-4970-9665-b43e316aca69
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 7%

---

# 작업 로그 세부 정보{#joblogdetailaux}

주 작업 로그 메시지와 관련된 보조 메시지(JobDetail)를 포함합니다. 현재 처리된 자산과 관련된 경고 및 기타 세부 정보를 포함합니다.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| logMessage | `xsd:string` | 보조 메시지. |
| logType | `xsd:string` | 로그 유형: `IPSJobLog.gcUploadWarning` 또는 `IPSJobLog.gcUploadError`. |
| dateCreated | `xsd:dateTime` | 보조 작업 로그 생성 날짜입니다. |
