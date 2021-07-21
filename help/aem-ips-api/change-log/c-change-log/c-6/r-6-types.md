---
description: IPS API 버전 6의 새로운 유형 및 변경된 유형에 대해 설명합니다.
solution: Experience Manager
title: 신규 및 수정된 데이터 유형
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d3bcd718-cf27-4d31-850f-a3205564be60
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 2%

---

# 데이터 유형: 신규 및 수정됨{#data-types-new-and-modified}

IPS API 버전 6의 새로운 유형 및 변경된 유형에 대해 설명합니다.

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

* `numUrls`을 `UploadUrlsJob`에 추가했습니다.

* `fileName`을 `Asset.`에 추가했습니다.

* `isHidden`을 `MetadataField`에 추가했습니다.

* `taskState`을 `TaskProgress`에 추가했습니다.

* `exportJob`을 `ActiveJob` 및 `ScheduledJob`에 추가했습니다.

* `optmizedPath` 및 `optimizedFile`을 `PsdInfo`에 추가했습니다.

* 다음에 `contextHandle`이 추가되었습니다.

   * `ImageRenderingPublishJob`
   * `VideoPublishJob`

* 다음 매개 변수를 `Asset`에 추가했습니다.

   * `animatedGifInfo`
   * `swcInfo`
   * `cssInfo`
   * `javascriptInfo`

**변경**

* `User`에서 `role`이 `defaultRole`(으)로 변경되었습니다.

* `Folder`에서 `permissions`이 `permissionsSetHandle`(으)로 변경되었습니다.

* `AssetSummary`에서 `type` 및 `name`는 이제 선택 사항입니다.
