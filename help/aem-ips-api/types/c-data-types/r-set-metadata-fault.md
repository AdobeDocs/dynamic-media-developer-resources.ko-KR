---
description: batchSetAssetMetadata 작업에서 사용 업데이트에 대한 경고 또는 오류 세부 사항입니다.
solution: Experience Manager
title: SetMetadataFault
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 49c6f355-4b5f-4b98-9a58-5732d56fdccb
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 12%

---

# SetMetadataFault{#setmetadatafault}

batchSetAssetMetadata 작업에서 사용 업데이트에 대한 경고 또는 오류 세부 사항입니다.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| assetHandle | `xsd:string` | 메타데이터가 설정되지 않은 자산입니다. |
| fieldHandle | `xsd:string` | 값이 설정되지 않은 메타데이터 필드의 핸들입니다. |
| 코드 | `xsd:int` | 오류 코드. |
| 이유 | `xsd:string` | 장애 설명(일반 텍스트). |
