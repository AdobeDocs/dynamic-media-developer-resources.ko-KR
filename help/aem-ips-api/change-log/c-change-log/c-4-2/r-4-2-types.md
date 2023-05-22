---
description: IPS API 버전 4.2의 새로운 데이터 형식과 변경된 데이터 형식을 설명합니다.
solution: Experience Manager
title: 새 데이터 유형 및 수정된 데이터 유형
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 3917e778-bd28-4047-b9f8-3063f136e492
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '51'
ht-degree: 1%

---

# 데이터 유형: 신규 및 수정됨{#data-types-new-and-modified}

IPS API 버전 4.2의 새로운 데이터 형식과 변경된 데이터 형식을 설명합니다.

구문

## 새 유형 {#section-770a814386a44478881feeff2b6f65f5}

* `AudioInfo`
* `CuePointInfo`
* `PdfSettings`
* `PremeierExpressRemixInfo`

## 수정된 유형 {#section-6c42b62dd91c4e9bb3a067b9abe3adee}

**자산**

추가된 매개 변수:

* `readyForPublish`
* `trashState`
* `MaskInfo`
* `RTFInfo`

제거된 매개 변수:

* `ImageSetInfo`
* `RenderSetInfo`

**AssetsJob 재처리**

추가된 매개 변수:

* `preservePublishState`
* `preserveCrop`
* `readyForPublish`

**업로드 디렉터리 작업**

추가된 매개 변수:

* `preservePublishState`
* `preserveCrop`
* `videoEncodingPreset`

**UploadUrlsJob**

추가된 매개 변수:

* `preservePublishState`
* `preserveCrop`
