---
description: IPS API 버전 4.4의 새로운 데이터 유형 및 변경된 데이터 유형에 대해 설명합니다.
solution: Experience Manager
title: 데이터 유형 새로 만들기 및 수정됨
feature: Dynamic Media Classic,SDK/API
role: 개발자,관리자
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 3%

---


# 데이터 유형:새로 만들기 및 수정됨{#data-types-new-and-modified}

IPS API 버전 4.4의 새로운 데이터 유형 및 변경된 데이터 유형에 대해 설명합니다.

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

## 수정된 형식 {#section-dfd062062ad444b0876bbc951fb1560c}

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

