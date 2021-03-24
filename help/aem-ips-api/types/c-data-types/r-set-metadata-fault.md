---
description: batchSetAssetMetadata 작업의 사용 업데이트에 대한 경고 또는 오류 세부 정보입니다.
solution: Experience Manager
title: SetMetadataFault
feature: Dynamic Media Classic,SDK/API,메타데이터
role: 개발자,관리자
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 10%

---


# SetMetadataFault{#setmetadatafault}

batchSetAssetMetadata 작업의 사용 업데이트에 대한 경고 또는 오류 세부 정보입니다.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| `*`assetHandle`*` | `xsd:string` | 메타데이터가 설정되지 않은 자산입니다. |
| `*`fieldHandle`*` | `xsd:string` | 값이 설정되지 않은 메타데이터 필드의 핸들입니다. |
| `*`코드`*` | `xsd:int` | 오류 코드. |
| `*`이유`*` | `xsd:string` | 오류 설명(일반 텍스트). |

