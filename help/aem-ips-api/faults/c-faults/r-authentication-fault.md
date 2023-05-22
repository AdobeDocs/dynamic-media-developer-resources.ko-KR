---
description: 사용자를 인증할 수 없을 때 발생합니다.
solution: Experience Manager
title: authenticationFault
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fce5c227-9291-4d17-801f-4ef4b8d43eb4
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '37'
ht-degree: 21%

---

# authenticationFault{#authenticationfault}

사용자를 인증할 수 없을 때 발생합니다.

구문

## 장애 유형 {#section-8ac4519c1dbb4c8b9c46ac9d1f44a054}

| ID | 오류 |
|---|---|
| 10000 | `AUTHENTICATION_FAULT_CODE_NO_CREDENTIALS` |
| 10001 | `AUTHENTICATION_FAULT_CODE_INVALID_CREDENTIALS` |
| 10002 | `AUTHENTICATION_FAULT_CODE_INVALID_USER` |

## 오류 필드 {#section-1fe84846a7154b03ab49552810ee9ac3}

| 이름 | 유형 | 설명 |
|---|---|---|
| `code` | `xsd:int` | 오류 ID |
| `reason` | `xsd:string` | 오류를 설명하는 정보 메시지. |
