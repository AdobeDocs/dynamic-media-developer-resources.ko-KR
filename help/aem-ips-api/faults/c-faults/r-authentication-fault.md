---
description: 사용자를 인증할 수 없을 때 발생합니다.
solution: Experience Manager
title: authenticationFault
feature: Dynamic Media Classic,SDK/API
role: 개발자,관리자
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 18%

---


# authenticationFault{#authenticationfault}

사용자를 인증할 수 없을 때 발생합니다.

구문

## 오류 유형 {#section-8ac4519c1dbb4c8b9c46ac9d1f44a054}

| ID | 오류 |
|---|---|
| 10000 | `AUTHENTICATION_FAULT_CODE_NO_CREDENTIALS` |
| 10001 | `AUTHENTICATION_FAULT_CODE_INVALID_CREDENTIALS` |
| 10002년 | `AUTHENTICATION_FAULT_CODE_INVALID_USER` |

## 오류 필드 {#section-1fe84846a7154b03ab49552810ee9ac3}

| 이름 | 유형 | 설명 |
|---|---|---|
| `code` | `xsd:int` | 오류 ID |
| `reason` | `xsd:string` | 결점을 설명하는 유용한 메시지입니다. |
