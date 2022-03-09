---
title: AssetMetadataFields
description: 지정된 자산 유형에 대한 메타데이터 필드 정의를 반환합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: ad2a45fc-1f30-4b8b-be7c-84cc60c7bd4b
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 10%

---

# AssetMetadataFields{#assetmetadatafields}

지정된 자산 유형에 대한 메타데이터 필드 정의를 반환합니다.

구문

## 매개 변수 {#section-5ad771540c5f40c187b35e34aac19305}

| 이름 | 유형 | 설명 |
|---|---|---|
| assetType | `xsd:string` | 필드 정의와 연결된 자산 유형(값에 대해서는 &quot;자산 유형&quot; 참조). |
| fieldArray | `types:MetadataFieldArray` | 에 지정된 자산 유형과 연관된 메타데이터 필드 정의 배열입니다. `assetType`. |
