---
description: IPS API 버전 6의 새로운 형식과 변경된 형식을 설명합니다.
solution: Experience Manager
title: 새 데이터 유형 및 수정된 데이터 유형
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d3bcd718-cf27-4d31-850f-a3205564be60
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 2%

---

# 데이터 유형: 신규 및 수정됨{#data-types-new-and-modified}

IPS API 버전 6의 새로운 형식과 변경된 형식을 설명합니다.

구문

## 새 유형 {#section-71ba6954339e4ba899acdf8a3212d6f3}

* `AssetContextStateUpdate`
* `AssetContextStateUpdateArray`
* `AssetPublishContexts`
* `AssetPublishContextsArray`
* `CompanyMember`
* `CompanyMemberArray`
* `CompanyMembershipUpdate`
* `CompanyMembershipUpdateArray`
* `ContextStateUpdate`
* `ContextStateUpdateArray`
* `Export Job`
* `PermissionsSet`
* `PermissionsSetArray`
* `PublishContext`
* `PublishContextArray`

## 수정된 유형 {#section-56b834b1a3b843279d8715b4a4f3890b}

**추가됨**

* 추가됨 `numUrls` 끝 `UploadUrlsJob`.

* 추가됨 `fileName` 끝 `Asset.`

* 추가됨 `isHidden` 끝 `MetadataField`.

* 추가됨 `taskState` 끝 `TaskProgress`.

* 추가됨 `exportJob` 끝 `ActiveJob` 및 `ScheduledJob`.

* 추가됨 `optmizedPath` 및 `optimizedFile` 끝 `PsdInfo`.

* 추가됨 `contextHandle` 끝:

   * `ImageRenderingPublishJob`
   * `VideoPublishJob`

* 에 다음 매개 변수를 추가했습니다. `Asset`:

   * `animatedGifInfo`
   * `swcInfo`
   * `cssInfo`
   * `javascriptInfo`

**변경**

* 위치 `User`, 변경됨 `role` 끝 `defaultRole`.

* 위치 `Folder`, 변경됨 `permissions` 끝 `permissionsSetHandle`.

* 위치 `AssetSummary`, `type` 및 `name` 이제 선택 사항입니다.
