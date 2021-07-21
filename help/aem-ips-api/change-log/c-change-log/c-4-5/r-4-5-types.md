---
description: IPS API 버전 4.5의 새로운 데이터 유형과 변경된 데이터 유형에 대해 설명합니다.
solution: Experience Manager
title: 신규 및 수정된 데이터 유형
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 45024d75-8058-40f8-b3e3-9b28b4cdc3f7
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 3%

---

# 데이터 유형: 신규 및 수정됨{#data-types-new-and-modified}

IPS API 버전 4.5의 새로운 데이터 유형과 변경된 데이터 유형에 대해 설명합니다.

구문

## 새 유형 {#section-6941b228cf6747a987e98c3d6e4b6b17}

* `AssetSummary`
* `AssetSummaryArray`
* `JobLogDetailAux`
* `JobLogDetailAuxArray`
* `MPEvent`
* `MPEventArray`
* `OperationFault`
* `OperationFaultArray`
* `PhotoshopOptions`
* `TagCondition`
* `TagConditionArray`
* `TagFieldValues`
* `TagFieldValuesArray`
* `TagValueUpdate`
* `TagValueUpdateArray`
* `TagValueUpdateFault`
* `TagValueUpdateFaultArray`
* `UrlArray`

## 수정된 유형 {#section-6ecdf752cc1a4636a583b4c546a0fccf}

* 자산에는 가상 파일 이름을 반환하는 새 `fileName` 필드가 포함되어 있습니다.
* `AssetSummary` 및  `type` 필드  `name` 반환

* `MetadataField` 포함 `isHidden`

* `MetadataUpdate`
* `UploadUrlsJob` 를 사용하려면  `urlArray` 및 선택적 카운트가  `numUrls` 필요합니다
