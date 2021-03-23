---
description: IPS API 버전 3.8의 새 작업 방법 및 변경된 작업 방법에 대해 설명합니다.
seo-description: IPS API 버전 3.8의 새 작업 방법 및 변경된 작업 방법에 대해 설명합니다.
seo-title: 작업 새로 만들기 및 수정됨
solution: Experience Manager
title: 작업 새로 만들기 및 수정됨
uuid: e836c5af-53b8-4bfa-a93a-98750cca9745
feature: Dynamic Media Classic,SDK/API
role: 개발자,관리자
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 1%

---


# 작업:새로 만들기 및 수정됨{#operations-new-and-modified}

IPS API 버전 3.8의 새 작업 방법 및 변경된 작업 방법에 대해 설명합니다.

구문

## 새 작업 {#section-64f0e4cd01154bb68c4e3e2dd8732ef5}

* `setAssetPublishState`
* `saveZoomTarget`
* `deleteZoomTarget`
* `saveImageMap`
* `deleteImageMap`
* `createImageSet`
* `getImageSetMembers`

## 수정한 작업 {#section-25eee732b69c49d0a27b1f3290f8654a}

**searchAssets**

* 선택적 `publishState` 매개 변수를 사용하여 `MarkedForPublish/NotMarkedForPublish` 자산 상태에서 검색할 수 있습니다.

**getJobLogs**

* 선택적 `userHandle` 매개 변수를 사용하면 특정 사용자가 제출한 작업 로그를 검색할 수 있습니다.

