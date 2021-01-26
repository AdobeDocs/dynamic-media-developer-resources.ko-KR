---
description: IPS API 버전 3.7의 새 작업 방법 및 변경된 작업 방법에 대해 설명합니다.
solution: Experience Manager
title: 작업 새로 만들기 및 수정됨
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 2%

---


# 작업:새로 만들기 및 수정됨{#operations-new-and-modified}

IPS API 버전 3.7의 새 작업 방법 및 변경된 작업 방법에 대해 설명합니다.

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

## 수정한 작업 {#section-596ea55a371e4c2ab5531e21ea9d8090}

**searchAsset**

* `name` 매개 변수를 제거했습니다.
* `excludeFieldArray`이(가) 추가되었습니다.

**getFolders**

* `excludeFieldArray`이(가) 추가되었습니다.

**getFolderTree**

* `excludeFieldArray` 및 `getUniqueMetadataValues`이(가) 추가되었습니다.
* `fieldHandle`이(가) 필수 매개 변수로 만들어졌습니다.

