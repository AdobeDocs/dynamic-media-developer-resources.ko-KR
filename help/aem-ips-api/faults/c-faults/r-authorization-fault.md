---
description: 인증된 사용자가 작업을 수행할 권한이 없을 때 발생합니다.
solution: Experience Manager
title: authorizationFault
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 27%

---


# authorizationFault{#authorizationfault}

인증된 사용자가 작업을 수행할 권한이 없을 때 발생합니다.

구문

## 오류 유형 {#section-1f04dec489714ee6bb7256fae6ab7730}

| ID | 오류 |
|---|---|
| 20000년 | `AUTHORIZATION_FAULT_CODE_INVALID_COMPANY` |
| 2001년 | `AUTHORIZATION_FAULT_CODE_INVALID_REQUEST_USERNAME` |
| 2002년 | `AUTHORIZATION_FAULT_CODE_INVALID_REQUEST_USER` |
| 2003년 | `AUTHORIZATION_FAULT_CODE_NO_OPERATION_PERMISSION` |
| 2004년 | `AUTHORIZATION_FAULT_CODE_NO_IMPERSONATION_PERMISSION` |
| 2005년 | `AUTHORIZATION_FAULT_CODE_ILLEGAL_PARAMETER_VALUE` |
| 2006년 | `AUTHORIZATION_FAULT_CODE_ILLEGAL_COMPANY` |
| 2007년 | `AUTHORIZATION_FAULT_CODE_ILLEGAL_REQUEST_USER` |
| 2008년 | `AUTHORIZATION_FAULT_CODE_ILLEGAL_ACCESS_GROUP` |
| 2009년 | `AUTHORIZATION_FAULT_CODE_MISSING_PERMISSION` |

## 오류 필드 {#section-4e3e41f41fea402a9ae314bfd05f663e}

| 이름 | 유형 | 설명 |
|---|---|---|
| `code` | `xsd:int` | 오류 ID |
| `reason` | `xsd:string` | 결점을 설명하는 유용한 메시지입니다. |

