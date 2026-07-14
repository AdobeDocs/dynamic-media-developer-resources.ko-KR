---
description: batchSetAssetMetadata 작업의 사용 업데이트에 대한 경고 또는 오류 세부 정보.
solution: Experience Manager
title: 메타데이터 오류 설정
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 49c6f355-4b5f-4b98-9a58-5732d56fdccb
TQID: 'https://experienceleague.adobe.com/kqC7eTmOZHNIYAn8yTKr-q-rJMQMzqBC9moArFK9no4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 83717f155466c1b33cab6f1f8830a9fea68c88c5
workflow-type: tm+mt
source-wordcount: 58
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

