---
description: 사용자를 인증할 수 없을 때 발생합니다.
seo-description: 사용자를 인증할 수 없을 때 발생합니다.
seo-title: authenticationFault
solution: Experience Manager
title: authenticationFault
topic: Scene7 Image Production System API
uuid: 89cc6f09-def6-4db1-a8b5-410909693dce
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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

## 장애 필드 {#section-1fe84846a7154b03ab49552810ee9ac3}

| 이름 | 유형 | 설명 |
|---|---|---|
| `code` | `xsd:int` | 장애 ID |
| `reason` | `xsd:string` | 단절을 설명하는 유용한 메시지입니다. |

