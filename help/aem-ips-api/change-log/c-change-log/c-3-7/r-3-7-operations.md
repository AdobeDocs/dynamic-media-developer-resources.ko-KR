---
description: IPS API 버전 3.7의 새 작업 방법 및 변경된 작업 방법에 대해 설명합니다.
seo-description: IPS API 버전 3.7의 새 작업 방법 및 변경된 작업 방법에 대해 설명합니다.
seo-title: 작업 새로 만들기 및 수정됨
solution: Experience Manager
title: 작업 새로 만들기 및 수정됨
topic: Scene7 Image Production System API
uuid: 3c163157-cd0d-4887-a1f0-7941d96c36f9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 1%

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

