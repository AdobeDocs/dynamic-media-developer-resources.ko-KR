---
description: IPS API 버전 4.4에 대한 새로운 데이터 형식과 변경된 데이터 형식을 설명합니다.
solution: Experience Manager
title: 새 데이터 유형 및 수정된 데이터 유형
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d8800b15-b9a3-4497-8b6b-fd318458ab5a
TQID: 'https://experienceleague.adobe.com/M6caMx5DHaAFtDj-feUVEOQeHgr2--5R9gKmkoeQB1g'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 4185012f22b173b569d11ea4d350763a82f98710
workflow-type: tm+mt
source-wordcount: 48
ht-degree: 2%

---

# 데이터 유형: 신규 및 수정됨{#data-types-new-and-modified}

IPS API 버전 4.4에 대한 새로운 데이터 형식과 변경된 데이터 형식을 설명합니다.

구문

## 새 유형 {#section-b910343aff304ec9b4d74045a2596a74}

* `AssetMetadataFields`
* `AssetMetadataFieldsArray`
* `AssetSetInfo`
* `AutoSetCreationOptions`
* `ExcludeByproductCondition`
* `ExcludeByproductArray`
* `FontFieldUpdate`
* `FontFieldUpdateArray`
* `IccProfileFieldUpdate`
* `IccProfileFieldUpdateArray`

## 수정된 유형 {#section-dfd062062ad444b0876bbc951fb1560c}

**자산**

추가된 매개 변수:

* `subtype`
* `assetSetInfo`

**작업 로그**

추가된 매개 변수:

* `transferSuccessCount`
* `transferErrorCount`
* `transferWarningCount`

**PDFInfo**

추가된 매개 변수:

* `extractLinks`

