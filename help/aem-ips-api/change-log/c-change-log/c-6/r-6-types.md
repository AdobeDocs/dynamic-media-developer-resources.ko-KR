---
description: IPS API 버전 6의 새로운 유형과 변경된 유형에 대해 설명합니다.
solution: Experience Manager
title: 데이터 유형 새로 만들기 및 수정됨
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 2%

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

## 수정된 형식 {#section-56b834b1a3b843279d8715b4a4f3890b}

**추가됨**

* `numUrls`을(를) `UploadUrlsJob`에 추가했습니다.

* `Asset.`에 `fileName`을(를) 추가했습니다.

* `isHidden`을(를) `MetadataField`에 추가했습니다.

* `taskState`을(를) `TaskProgress`에 추가했습니다.

* `exportJob`을(를) `ActiveJob` 및 `ScheduledJob`에 추가했습니다.

* `optmizedPath` 및 `optimizedFile`을(를) `PsdInfo`에 추가했습니다.

* 다음에 `contextHandle`을(를) 추가했습니다.

   * `ImageRenderingPublishJob`
   * `VideoPublishJob`

* 다음 매개 변수를 `Asset`에 추가했습니다.

   * `animatedGifInfo`
   * `swcInfo`
   * `cssInfo`
   * `javascriptInfo`

**변경**

* `User`에서 `role`을(를) `defaultRole`(으)로 변경했습니다.

* `Folder`에서 `permissions`을(를) `permissionsSetHandle`(으)로 변경했습니다.

* 이제 `AssetSummary`에서 `type` 및 `name`는 선택 사항입니다.

