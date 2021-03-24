---
description: ipsApiFault
solution: Experience Manager
title: ipsApiFault
feature: Dynamic Media Classic,SDK/API
role: 개발자,관리자
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '32'
ht-degree: 28%

---


# ipsApiFault{#ipsapifault}

구문

## 오류 유형 {#section-425697675cac4b2ab5c48bd463956401}

| ID | 오류 |
|---|---|
| 30000 | `IPS_API_FAULT_CODE_EXCEPTION` |
| 30001 | `IPS_API_FAULT_CODE_INVALID_PARAMETER` |
| 30002 | `IPS_API_FAULT_CODE_MISSING_PARAMETER` |
| 30003 | `IPS_API_FAULT_CODE_INVALID_REQUEST_XML` |

## 오류 필드 {#section-37fe1aef1d5f4ca480071ca933aba826}

| 이름 | 유형 | 설명 |
|---|---|---|
| `code` | `xsd:int` | 오류 ID |
| `reason` | `xsd:string` | 결점을 설명하는 유용한 메시지입니다. |

