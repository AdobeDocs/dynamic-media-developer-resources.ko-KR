---
description: 일괄 처리 자산 작업 중에 생성된 경고 또는 오류 조건에 대한 정보를 포함합니다. 코드 및 사유 필드는 동일한 비배치 작업에 대해 throw될 오류 메시지 필드에 해당합니다.
seo-description: 일괄 처리 자산 작업 중에 생성된 경고 또는 오류 조건에 대한 정보를 포함합니다. 코드 및 사유 필드는 동일한 비배치 작업에 대해 throw될 오류 메시지 필드에 해당합니다.
seo-title: AssetOperationFault
solution: Experience Manager
title: AssetOperationFault
uuid: fb6c5482-6e16-4561-927b-e4daeb7bdd7b
feature: Dynamic Media Classic,SDK/API,자산 관리
role: 개발자,관리자
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 5%

---


# AssetOperationFault{#assetoperationfault}

일괄 처리 자산 작업 중에 생성된 경고 또는 오류 조건에 대한 정보를 포함합니다. 코드 및 사유 필드는 동일한 비배치 작업에 대해 throw될 오류 메시지 필드에 해당합니다.

구문

## 매개 변수 {#section-c906f052f43e4785ba46d92b514b0923}

| 이름 | 유형 | 설명 |
|---|---|---|
| `*`assetHandle`*` | `xsd:string` | 실패한 작업에 대한 자산 핸들입니다. |
| `*`코드`*` | `xsd:int` | 작업 오류 코드. |
| `*`이유`*` | `xsd:string` | 오류 설명 또는 이유 |

