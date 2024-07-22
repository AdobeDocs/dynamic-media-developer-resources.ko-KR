---
description: IPS API 버전 6에 대한 새로운 작업 및 변경된 작업 방법을 설명합니다.
solution: Experience Manager
title: 새 작업 및 수정된 작업
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fc7af77e-17fc-453a-8949-78c9c5c33b34
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 1%

---

# 작업: 신규 및 수정됨{#operations-new-and-modified}

IPS API 버전 6에 대한 새로운 작업 및 변경된 작업 방법을 설명합니다.

구문

## 새 작업 {#section-088502a0746945f28a5ea100cd655bc6}

* `batchGetAssetPublishContexts`
* `getPublishContexts`
* `moveFolder`
* `setAssetsContexState`
* `updateAssetSet`
* `updateImageSet`

## 수정된 작업 {#section-f4e8755527444266ae806e3f4c851ae6}

**추가됨**

* `isHidden` 및 `initialTagValue`이(가) 다음에 추가됨:

   * `saveMetadataField`
   * ` `updateMetadataField&quot;
   * `createMetadataField`

* `thumbAssetHandle`이(가) 다음에 추가됨:

   * `createImageSet`
   * `createAssetSet`

  `companyHandle`이(가) 다음에 추가됨:

   * `getViewerConfigSettings`
   * `setViewerConfigSettings`
   * `updateViewerConfigSettings`
   * `getSearchStrings`

  `contextHandle`이(가) 다음에 추가됨:

   * `getImageServingPublishSettings`
   * `getImageRenderingPublishSettings`
   * `setImageServingPublishSettings`
   * `setImageRenderingPublishSettings`

* includeInactive가 다음에 추가됨:

   * `getUsers`.
   * `getUserChars`.

* `createPropertySet`에 `permissionArray`을(를) 추가했습니다.

* `submitJob`에 `exportJob`을(를) 추가했습니다.

**변경됨**

* `addUser` 및 `setUser`에서 `role`을(를) `defaultRole`(으)로 변경했습니다.

* `getCompanyMembers`에서 `userArray`을(를) `memberArray`(으)로 변경했습니다.

* `getCompanyMembership`에서 `companyArray`을(를) `membershipArray`(으)로 변경했습니다.

* `addUser`, `setCompanyMembership` 및 `addCompanyMembership`에서 `membershipArray`을(를) `companyHandleArray`(으)로 변경했습니다.

* `getCompanyMembership`에서 `companyArray`을(를) `membershipArray`(으)로 변경했습니다.

* `getUserChars`에서 `includeInvalid`은(는) 이제 선택 사항입니다.

**제거됨**

* `renameAsset`에서 `renameFiles`을(를) 제거했습니다.

* `getXMPPanelViewDefinition`을(를) 제거했습니다.
* `searchAssetsByFulltext` 및 `searchAssetsBySimilarity`을(를) 제거했습니다.
