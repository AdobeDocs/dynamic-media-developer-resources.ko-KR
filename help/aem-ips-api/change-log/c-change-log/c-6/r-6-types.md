---
description: IPS API 버전 6의 새로운 형식과 변경된 형식을 설명합니다.
solution: Experience Manager
title: 새 데이터 유형 및 수정된 데이터 유형
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d3bcd718-cf27-4d31-850f-a3205564be60
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 1%

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

* `numUrls`에 `UploadUrlsJob`을(를) 추가했습니다.

* `fileName`에 `Asset.`을(를) 추가함

* `isHidden`에 `MetadataField`을(를) 추가했습니다.

* `taskState`에 `TaskProgress`을(를) 추가했습니다.

* `exportJob` 및 `ActiveJob`에 `ScheduledJob`을(를) 추가했습니다.

* `optmizedPath`에 `optimizedFile` 및 `PsdInfo`을(를) 추가했습니다.

* `contextHandle`이(가) 다음에 추가됨:

   * `ImageRenderingPublishJob`
   * `VideoPublishJob`

* `Asset`에 다음 매개 변수를 추가했습니다.

   * `animatedGifInfo`
   * `swcInfo`
   * `cssInfo`
   * `javascriptInfo`

**변경됨**

* `User`에서 `role`을(를) `defaultRole`(으)로 변경했습니다.

* `Folder`에서 `permissions`을(를) `permissionsSetHandle`(으)로 변경했습니다.

* `AssetSummary`에서 `type` 및 `name`은(는) 이제 선택 사항입니다.
