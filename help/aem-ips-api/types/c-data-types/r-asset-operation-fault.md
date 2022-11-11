---
title: AssetOperationFault
description: 배치 자산 작업 중에 생성된 경고 또는 오류 조건에 대한 정보를 포함합니다. 코드 및 이유 필드는 동일한 일괄 처리가 아닌 작업에 대해 throw되었을 오류 메시지 필드에 해당합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: c97fc35b-76f8-4ff7-a1ae-e5f9749f376c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 7%

---

# [!DNL AssetOperationFault]{#assetoperationfault}

배치 자산 작업 중에 생성된 경고 또는 오류 조건에 대한 정보를 포함합니다. 코드 및 이유 필드는 동일한 일괄 처리가 아닌 작업에 대해 throw되었을 오류 메시지 필드에 해당합니다.

구문

## 매개 변수 {#section-c906f052f43e4785ba46d92b514b0923}

| 이름 | 유형 | 설명 |
|---|---|---|
| assetHandle | `xsd:string` | 실패한 작업에 대한 자산 핸들입니다. |
| 코드 | `xsd:int` | 작업 오류 코드. |
| 이유 | `xsd:string` | 오류 설명 또는 이유 |
