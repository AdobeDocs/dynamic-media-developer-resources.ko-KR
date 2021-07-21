---
description: IPS API 버전 4.4의 새로운 데이터 유형과 변경된 데이터 유형에 대해 설명합니다.
solution: Experience Manager
title: 신규 및 수정된 데이터 유형
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d8800b15-b9a3-4497-8b6b-fd318458ab5a
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '51'
ht-degree: 3%

---

# 데이터 유형: 신규 및 수정됨{#data-types-new-and-modified}

IPS API 버전 4.4의 새로운 데이터 유형과 변경된 데이터 유형에 대해 설명합니다.

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
