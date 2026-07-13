---
title: 에셋 메타데이터 필드
description: 지정된 에셋 유형에 대한 메타데이터 필드 정의를 반환합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: ad2a45fc-1f30-4b8b-be7c-84cc60c7bd4b
TQID: 'https://experienceleague.adobe.com/U9JVe27HBTMtlBXmwDnkVAOaVfsBspa5r5fvnQl-h58'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: b658a9f9067d2313c1c838c7e157f4070ebc2b50
workflow-type: tm+mt
source-wordcount: 47
ht-degree: 10%

---

# [!DNL AssetMetadataFields]{#assetmetadatafields}

지정된 에셋 유형에 대한 메타데이터 필드 정의를 반환합니다.

구문

## 매개 변수 {#section-5ad771540c5f40c187b35e34aac19305}

| 이름 | 유형 | 설명 |
|---|---|---|
| assetType | `xsd:string` | 필드 정의와 연결된 에셋 유형(값에 대한 &quot;에셋 유형&quot; 참조). |
| fieldArray | `types:MetadataFieldArray` | `assetType`에 지정된 에셋 유형과 연결된 메타데이터 필드 정의의 배열입니다. |

