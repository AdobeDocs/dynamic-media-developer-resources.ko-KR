---
description: 기본 작업 로그 메시지(JobDetail)와 관련된 보조 메시지를 포함합니다. 현재 처리된 에셋과 관련된 경고 및 기타 세부 정보를 포함합니다.
solution: Experience Manager
title: JobLogDetailAux
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 789736c5-d74d-4970-9665-b43e316aca69
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 7%

---

# [!DNL JobLogDetailAux]{#joblogdetailaux}

기본 작업 로그 메시지(JobDetail)와 관련된 보조 메시지를 포함합니다. 현재 처리된 에셋과 관련된 경고 및 기타 세부 정보를 포함합니다.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| logMessage | `xsd:string` | 보조 메시지. |
| logType | `xsd:string` | 로그 유형: `IPSJobLog.gcUploadWarning` 또는 `IPSJobLog.gcUploadError`. |
| dateCreated | `xsd:dateTime` | 보조 작업 로그 생성 날짜입니다. |
