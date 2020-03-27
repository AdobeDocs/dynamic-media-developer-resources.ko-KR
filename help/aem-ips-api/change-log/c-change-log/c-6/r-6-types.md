---
description: IPS API 버전 6의 새로운 유형과 변경된 유형에 대해 설명합니다.
seo-description: IPS API 버전 6의 새로운 유형과 변경된 유형에 대해 설명합니다.
seo-title: 데이터 유형 새로 만들기 및 수정됨
solution: Experience Manager
title: 데이터 유형 새로 만들기 및 수정됨
topic: Scene7 Image Production System API
uuid: ef7c43ee-467f-46b9-bd82-05e8359bd829
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 데이터 유형:새로 만들기 및 수정됨{#data-types-new-and-modified}

IPS API 버전 6의 새로운 유형과 변경된 유형에 대해 설명합니다.

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

* 에 `numUrls` 추가되었습니다 `UploadUrlsJob`.

* 에 `fileName` 추가됨 `Asset.`

* 에 `isHidden` 추가되었습니다 `MetadataField`.

* 에 `taskState` 추가되었습니다 `TaskProgress`.

* 및 `exportJob` 에 `ActiveJob` 추가되었습니다 `ScheduledJob`.

* 에 `optmizedPath` 및 `optimizedFile` 을 `PsdInfo`추가했습니다.

* 추가된 `contextHandle` 위치:

   * `ImageRenderingPublishJob`
   * `VideoPublishJob`

* 다음 매개 변수를 `Asset`추가했습니다.

   * `animatedGifInfo`
   * `swcInfo`
   * `cssInfo`
   * `javascriptInfo`

**변경**

* 에서 `User`로 `role` `defaultRole`변경되었습니다.

* 에서 `Folder`로 `permissions` `permissionsSetHandle`변경되었습니다.

* in `AssetSummary`및 `type` `name` 이제 선택 사항입니다.

