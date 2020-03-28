---
description: batchSetAssetMetadata 작업의 사용 업데이트에 대한 경고 또는 오류 세부 정보입니다.
seo-description: batchSetAssetMetadata 작업의 사용 업데이트에 대한 경고 또는 오류 세부 정보입니다.
seo-title: SetMetadataFault
solution: Experience Manager
title: SetMetadataFault
topic: Scene7 Image Production System API
uuid: 22302bb0-914a-4d50-a188-9c3ee58e0481
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SetMetadataFault{#setmetadatafault}

batchSetAssetMetadata 작업의 사용 업데이트에 대한 경고 또는 오류 세부 정보입니다.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| ` *`assetHandle`*` | `xsd:string` | 메타데이터가 설정되지 않은 자산입니다. |
| ` *`fieldHandle`*` | `xsd:string` | 값이 설정되지 않은 메타데이터 필드의 핸들입니다. |
| ` *`코드`*` | `xsd:int` | 오류 코드. |
| ` *`이유`*` | `xsd:string` | 오류 설명(일반 텍스트). |

