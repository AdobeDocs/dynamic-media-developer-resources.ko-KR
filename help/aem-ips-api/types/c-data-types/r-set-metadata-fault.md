---
description: batchSetAssetMetadata 작업의 사용 업데이트에 대한 경고 또는 오류 세부 정보.
solution: Experience Manager
title: 메타데이터 오류 설정
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 49c6f355-4b5f-4b98-9a58-5732d56fdccb
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 12%

---

# [!DNL SetMetadataFault]{#setmetadatafault}

batchSetAssetMetadata 작업의 사용 업데이트에 대한 경고 또는 오류 세부 정보.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| assetHandle | `xsd:string` | 메타데이터가 설정되지 않은 에셋입니다. |
| 필드 핸들 | `xsd:string` | 값이 설정되지 않은 메타데이터 필드에 대한 핸들입니다. |
| 코드 | `xsd:int` | 오류 코드. |
| 이유 | `xsd:string` | 오류 설명(일반 텍스트). |
