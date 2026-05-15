---
description: IPS API 버전 6의 새로운 형식과 변경된 형식을 설명합니다.
solution: Experience Manager
title: 새 데이터 유형 및 수정된 데이터 유형
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d3bcd718-cf27-4d31-850f-a3205564be60
TQID: 'https://experienceleague.adobe.com/LI8xzlS2eACzYqcV3krzThLm77-z6imYLohPRCTHIYs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 71
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

* `UploadUrlsJob`에 `numUrls`을(를) 추가했습니다.

* `Asset.`에 `fileName`을(를) 추가함

* `MetadataField`에 `isHidden`을(를) 추가했습니다.

* `TaskProgress`에 `taskState`을(를) 추가했습니다.

* `ActiveJob` 및 `ScheduledJob`에 `exportJob`을(를) 추가했습니다.

* `PsdInfo`에 `optmizedPath` 및 `optimizedFile`을(를) 추가했습니다.

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
