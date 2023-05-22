---
title: 에셋 메타데이터 필드
description: 지정된 에셋 유형에 대한 메타데이터 필드 정의를 반환합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: ad2a45fc-1f30-4b8b-be7c-84cc60c7bd4b
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '47'
ht-degree: 10%

---

# [!DNL AssetMetadataFields]{#assetmetadatafields}

지정된 에셋 유형에 대한 메타데이터 필드 정의를 반환합니다.

구문

## 매개 변수 {#section-5ad771540c5f40c187b35e34aac19305}

| 이름 | 유형 | 설명 |
|---|---|---|
| assetType | `xsd:string` | 필드 정의와 연결된 에셋 유형(값에 대한 &quot;에셋 유형&quot; 참조). |
| fieldArray | `types:MetadataFieldArray` | 에 지정된 에셋 유형과 연결된 메타데이터 필드 정의의 배열 `assetType`. |
