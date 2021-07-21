---
description: IPS API 버전 6에 대한 새로운 작업 및 변경된 작업 방법에 대해 설명합니다.
solution: Experience Manager
title: 새 작업 및 수정된 작업
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fc7af77e-17fc-453a-8949-78c9c5c33b34
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 2%

---

# 작업: 신규 및 수정됨{#operations-new-and-modified}

IPS API 버전 6에 대한 새로운 작업 및 변경된 작업 방법에 대해 설명합니다.

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

* 다음 항목에 `isHidden` 및 `initialTagValue`이 추가되었습니다.

   * `saveMetadataField`
   * ` `updateMetadataField&quot;
   * `createMetadataField`

* 다음에 `thumbAssetHandle`이 추가되었습니다.

   * `createImageSet`
   * `createAssetSet`

   다음에 `companyHandle`이 추가되었습니다.

   * `getViewerConfigSettings`
   * `setViewerConfigSettings`
   * `updateViewerConfigSettings`
   * `getSearchStrings`

   다음에 `contextHandle`이 추가되었습니다.

   * `getImageServingPublishSettings`
   * `getImageRenderingPublishSettings`
   * `setImageServingPublishSettings`
   * `setImageRenderingPublishSettings`



* inactive에 includeInactive가 추가되었습니다.

   * `getUsers`.
   * `getUserChars`.

* `permissionArray`을 `createPropertySet`에 추가했습니다.

* `exportJob`을 `submitJob`에 추가했습니다.

**변경**

* `addUser` 및 `setUser`에서 `role`가 `defaultRole`(으)로 변경되었습니다.

* `getCompanyMembers`에서 `userArray`이 `memberArray`(으)로 변경되었습니다.

* `getCompanyMembership`에서 `companyArray`이 `membershipArray`(으)로 변경되었습니다.

* `addUser`, `setCompanyMembership` 및 `addCompanyMembership`에서 `membershipArray`이 `companyHandleArray`로 변경되었습니다.

* `getCompanyMembership`에서 `companyArray`이 `membershipArray`(으)로 변경되었습니다.

* `getUserChars`에서 `includeInvalid`은 이제 선택 사항입니다.

**제거됨**

* `renameAsset`에서 `renameFiles`이(가) 제거되었습니다.

* `getXMPPanelViewDefinition`이(가) 제거되었습니다.
* `searchAssetsByFulltext` 및 `searchAssetsBySimilarity`이(가) 제거되었습니다.
