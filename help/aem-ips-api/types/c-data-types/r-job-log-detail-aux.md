---
description: 기본 작업 로그 메시지(JobDetail)와 관련된 보조 메시지를 포함합니다. 현재 처리된 에셋과 관련된 경고 및 기타 세부 정보를 포함합니다.
solution: Experience Manager
title: JobLogDetailAux
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 789736c5-d74d-4970-9665-b43e316aca69
TQID: 'https://experienceleague.adobe.com/Hl3L69Hd6Hm8acRaPgFVQCfo8PffGCn5fNGxthmStFM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 64
ht-degree: 7%

---

# [!DNL JobLogDetailAux]{#joblogdetailaux}

기본 작업 로그 메시지(JobDetail)와 관련된 보조 메시지를 포함합니다. 현재 처리된 에셋과 관련된 경고 및 기타 세부 정보를 포함합니다.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| logMessage | `xsd:string` | 보조 메시지. |
| logType | `xsd:string` | 로그 형식: `IPSJobLog.gcUploadWarning` 또는 `IPSJobLog.gcUploadError`. |
| dateCreated | `xsd:dateTime` | 보조 작업 로그 생성 날짜입니다. |
