---
description: IPS API 버전 3.7에 대한 새로운 작업 및 변경된 작업 방법에 대해 설명합니다.
solution: Experience Manager
title: 새 작업 및 수정된 작업
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 1f11a686-7239-4922-a608-5330864184ac
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 1%

---

# 작업:신규 및 수정됨{#operations-new-and-modified}

IPS API 버전 3.7에 대한 새로운 작업 및 변경된 작업 방법에 대해 설명합니다.

구문

## 새 작업 {#section-c4d34a58f8194d548fbe26ab3764ea58}

* `moveAsset`
* `renameAsset`
* `deleteAsset`
* `createFolder`
* `deleteFolder`
* `getActiveJobs`
* `getScheduledJobs`
* `getJobLogs`
* `getJbLogDetails`
* `submitJob`
* `stopJob`
* `pauseJob`
* `resumeJob`
* `executeJob`
* `deleteJob`

## 수정된 작업 {#section-596ea55a371e4c2ab5531e21ea9d8090}

**searchAsset**

* `name` 매개 변수가 제거되었습니다.
* `excludeFieldArray`을 추가했습니다.

**getFolders**

* `excludeFieldArray`을 추가했습니다.

**getFolderTree**

* `excludeFieldArray` 및 `getUniqueMetadataValues`을 추가했습니다.
* `fieldHandle`에 필요한 매개 변수가 작성되었습니다.
