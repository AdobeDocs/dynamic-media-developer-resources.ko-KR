---
description: 널
seo-description: 널
seo-title: ipsApiFault
solution: Experience Manager
title: ipsApiFault
topic: Scene7 Image Production System API
uuid: 010814a8-1d29-4b02-8449-cb26e4335e07
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ipsApiFault{#ipsapifault}

구문

## 장애 유형 {#section-425697675cac4b2ab5c48bd463956401}

| ID | 오류 |
|---|---|
| 30000 | `IPS_API_FAULT_CODE_EXCEPTION` |
| 30001 | `IPS_API_FAULT_CODE_INVALID_PARAMETER` |
| 30002 | `IPS_API_FAULT_CODE_MISSING_PARAMETER` |
| 30003 | `IPS_API_FAULT_CODE_INVALID_REQUEST_XML` |

## 장애 필드 {#section-37fe1aef1d5f4ca480071ca933aba826}

| 이름 | 유형 | 설명 |
|---|---|---|
| `code` | `xsd:int` | 장애 ID |
| `reason` | `xsd:string` | 단절을 설명하는 유용한 메시지입니다. |

