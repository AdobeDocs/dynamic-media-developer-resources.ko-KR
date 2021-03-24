---
description: 지정된 자산 유형에 대한 메타데이터 필드 정의를 반환합니다.
solution: Experience Manager
title: AssetMetadataFields
feature: Dynamic Media Classic,SDK/API,메타데이터,자산 관리
role: 개발자,관리자
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '58'
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

