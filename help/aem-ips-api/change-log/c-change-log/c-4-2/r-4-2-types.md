---
description: IPS API 버전 4.2의 새로운 데이터 유형 및 변경된 데이터 유형에 대해 설명합니다.
solution: Experience Manager
title: 데이터 유형 새로 만들기 및 수정됨
feature: Dynamic Media Classic,SDK/API
role: 개발자,관리자
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '58'
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

