---
title: AssetOperationFault
description: 자산 일괄 처리 작업 중 생성된 경고 또는 오류 조건에 대한 정보를 포함합니다. 코드 및 이유 필드는 동일한 비일괄 처리 작업을 위해 throw되었을 오류 메시지 필드에 해당합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: c97fc35b-76f8-4ff7-a1ae-e5f9749f376c
TQID: 'https://experienceleague.adobe.com/LCiMAp-8grDIfCEGX3sF2kBhDamlxZ8iFHT1BjBLkCY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 92
ht-degree: 7%

---

# [!DNL AssetOperationFault]{#assetoperationfault}

자산 일괄 처리 작업 중 생성된 경고 또는 오류 조건에 대한 정보를 포함합니다. 코드 및 이유 필드는 동일한 비일괄 처리 작업을 위해 throw되었을 오류 메시지 필드에 해당합니다.

구문

## 매개 변수 {#section-c906f052f43e4785ba46d92b514b0923}

| 이름 | 유형 | 설명 |
|---|---|---|
| assetHandle | `xsd:string` | 실패한 작업에 대한 에셋 핸들입니다. |
| 코드 | `xsd:int` | 작업 오류 코드. |
| 이유 | `xsd:string` | 오류 설명 또는 이유. |
