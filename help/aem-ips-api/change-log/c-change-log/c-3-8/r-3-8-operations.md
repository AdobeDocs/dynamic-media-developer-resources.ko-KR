---
description: IPS API 버전 3.8에 대한 새로운 작업 및 변경된 작업 방법에 대해 설명합니다.
solution: Experience Manager
title: 새 작업 및 수정된 작업
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 8f4fe698-afe8-4ce6-904d-42fa67dee4dd
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 1%

---

# 작업:신규 및 수정됨{#operations-new-and-modified}

IPS API 버전 3.8에 대한 새로운 작업 및 변경된 작업 방법에 대해 설명합니다.

구문

## 새 작업 {#section-64f0e4cd01154bb68c4e3e2dd8732ef5}

* `setAssetPublishState`
* `saveZoomTarget`
* `deleteZoomTarget`
* `saveImageMap`
* `deleteImageMap`
* `createImageSet`
* `getImageSetMembers`

## 수정된 작업 {#section-25eee732b69c49d0a27b1f3290f8654a}

**searchAssets**

* 선택 사항인 `publishState` 매개 변수를 사용하여 `MarkedForPublish/NotMarkedForPublish` 자산 상태를 검색할 수 있습니다.

**getJobLogs**

* 선택적 `userHandle` 매개 변수를 사용하면 특정 사용자가 제출한 작업 로그를 검색할 수 있습니다.
