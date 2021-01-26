---
description: IPS API 버전 4.2의 새로운 데이터 유형 및 변경된 데이터 유형에 대해 설명합니다.
solution: Experience Manager
title: 데이터 유형 새로 만들기 및 수정됨
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '51'
ht-degree: 3%

---


# 데이터 유형:새로 만들기 및 수정됨{#data-types-new-and-modified}

IPS API 버전 4.2의 새로운 데이터 유형 및 변경된 데이터 유형에 대해 설명합니다.

구문

## 새 유형 {#section-770a814386a44478881feeff2b6f65f5}

* `AudioInfo`
* `CuePointInfo`
* `PdfSettings`
* `PremeierExpressRemixInfo`

## 수정된 형식 {#section-6c42b62dd91c4e9bb3a067b9abe3adee}

**자산**

추가된 매개 변수:

* `readyForPublish`
* `trashState`
* `MaskInfo`
* `RTFInfo`

제거된 매개 변수:

* `ImageSetInfo`
* `RenderSetInfo`

**ReprocessAssetsJob**

추가된 매개 변수:

* `preservePublishState`
* `preserveCrop`
* `readyForPublish`

**UploadDirectoryJob**

추가된 매개 변수:

* `preservePublishState`
* `preserveCrop`
* `videoEncodingPreset`

**UploadUrlJob**

추가된 매개 변수:

* `preservePublishState`
* `preserveCrop`

