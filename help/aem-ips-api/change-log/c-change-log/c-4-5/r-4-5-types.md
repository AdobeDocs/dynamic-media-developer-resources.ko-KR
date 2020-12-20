---
description: IPS API 버전 4.5의 새로운 데이터 유형 및 변경된 데이터 유형에 대해 설명합니다.
seo-description: IPS API 버전 4.5의 새로운 데이터 유형 및 변경된 데이터 유형에 대해 설명합니다.
seo-title: 데이터 유형 새로 만들기 및 수정됨
solution: Experience Manager
title: 데이터 유형 새로 만들기 및 수정됨
topic: Scene7 Image Production System API
uuid: 2752f9dd-ec47-45d6-a465-6d275ec2b2fb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 2%

---


# 데이터 유형:새로 만들기 및 수정됨{#data-types-new-and-modified}

IPS API 버전 4.5의 새로운 데이터 유형 및 변경된 데이터 유형에 대해 설명합니다.

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

## 수정된 형식 {#section-6ecdf752cc1a4636a583b4c546a0fccf}

* 자산에 가상 파일 이름을 반환하는 새 `fileName` 필드가 포함되어 있습니다.
* `AssetSummary` 및  `type` 필드를  `name` 반환합니다.

* `MetadataField` 포함 `isHidden`

* `MetadataUpdate`
* `UploadUrlsJob` 필수  `urlArray` 항목 및 추가  `numUrls` 횟수

