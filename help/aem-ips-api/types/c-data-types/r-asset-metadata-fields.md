---
description: 지정된 자산 유형에 대한 메타데이터 필드 정의를 반환합니다.
seo-description: 지정된 자산 유형에 대한 메타데이터 필드 정의를 반환합니다.
seo-title: AssetMetadataFields
solution: Experience Manager
title: AssetMetadataFields
topic: Dynamic Media Image Production System API
uuid: aefb734c-7609-4227-ae2c-48a1469740ec
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 8%

---


# AssetMetadataFields{#assetmetadatafields}

지정된 자산 유형에 대한 메타데이터 필드 정의를 반환합니다.

구문

## 매개 변수 {#section-5ad771540c5f40c187b35e34aac19305}

| 이름 | 유형 | 설명 |
|---|---|---|
| `*`assetType`*` | `xsd:string` | 필드 정의와 연결된 자산 유형(값에 대한 자세한 내용은 &quot;자산 유형&quot; 참조). |
| `*`fieldArray`*` | `types:MetadataFieldArray` | `assetType`에 지정된 자산 유형과 연결된 메타데이터 필드 정의 배열입니다. |

