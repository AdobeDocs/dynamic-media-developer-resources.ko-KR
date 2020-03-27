---
description: 인증된 사용자에게 작업을 수행할 수 있는 권한이 없을 때 발생합니다.
seo-description: 인증된 사용자에게 작업을 수행할 수 있는 권한이 없을 때 발생합니다.
seo-title: authorizationFault
solution: Experience Manager
title: authorizationFault
topic: Scene7 Image Production System API
uuid: 8b8df22a-aa76-4cbd-9c14-89969c5f9620
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# authorizationFault{#authorizationfault}

인증된 사용자에게 작업을 수행할 수 있는 권한이 없을 때 발생합니다.

구문

## 장애 유형 {#section-1f04dec489714ee6bb7256fae6ab7730}

| ID | 오류 |
|---|---|
| 20000 | `AUTHORIZATION_FAULT_CODE_INVALID_COMPANY` |
| 20001 | `AUTHORIZATION_FAULT_CODE_INVALID_REQUEST_USERNAME` |
| 20002 | `AUTHORIZATION_FAULT_CODE_INVALID_REQUEST_USER` |
| 20003 | `AUTHORIZATION_FAULT_CODE_NO_OPERATION_PERMISSION` |
| 20004 | `AUTHORIZATION_FAULT_CODE_NO_IMPERSONATION_PERMISSION` |
| 20005 | `AUTHORIZATION_FAULT_CODE_ILLEGAL_PARAMETER_VALUE` |
| 20006 | `AUTHORIZATION_FAULT_CODE_ILLEGAL_COMPANY` |
| 20007 | `AUTHORIZATION_FAULT_CODE_ILLEGAL_REQUEST_USER` |
| 20008 | `AUTHORIZATION_FAULT_CODE_ILLEGAL_ACCESS_GROUP` |
| 20009 | `AUTHORIZATION_FAULT_CODE_MISSING_PERMISSION` |

## 장애 필드 {#section-4e3e41f41fea402a9ae314bfd05f663e}

| 이름 | 유형 | 설명 |
|---|---|---|
| `code` | `xsd:int` | 장애 ID |
| `reason` | `xsd:string` | 단절을 설명하는 유용한 메시지입니다. |

