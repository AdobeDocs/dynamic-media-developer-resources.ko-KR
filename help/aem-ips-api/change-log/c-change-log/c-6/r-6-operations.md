---
description: IPS API 버전 6의 새로운 작업 방법 및 변경된 작업 방법에 대해 설명합니다.
seo-description: IPS API 버전 6의 새로운 작업 방법 및 변경된 작업 방법에 대해 설명합니다.
seo-title: 작업 새로 만들기 및 수정됨
solution: Experience Manager
title: 작업 새로 만들기 및 수정됨
topic: Scene7 Image Production System API
uuid: e36f0d5c-0170-4a65-9347-c7fd3538726b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 작업:새로 만들기 및 수정됨{#operations-new-and-modified}

IPS API 버전 6의 새로운 작업 방법 및 변경된 작업 방법에 대해 설명합니다.

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

* 추가 `isHidden` 및 `initialTagValue` 대상:

   * `saveMetadataField`
   * ` `updateMetadataField&quot;
   * `createMetadataField`

* 추가된 `thumbAssetHandle` 위치:

   * `createImageSet`
   * `createAssetSet`
   추가된 `companyHandle` 위치:

   * `getViewerConfigSettings`
   * `setViewerConfigSettings`
   * `updateViewerConfigSettings`
   * `getSearchStrings`
   추가된 `contextHandle` 위치:

   * `getImageServingPublishSettings`
   * `getImageRenderingPublishSettings`
   * `setImageServingPublishSettings`
   * `setImageRenderingPublishSettings`



* includeInactive가 추가된 대상:

   * `getUsers`.
   * `getUserChars`.

* 에 `permissionArray` 추가되었습니다 `createPropertySet`.

* 에 `exportJob` 추가되었습니다 `submitJob`.

**변경**

* 인 `addUser` 및 `setUser`으로 `role` `defaultRole`변경되었습니다.

* 에서 `getCompanyMembers`로 `userArray` `memberArray`변경되었습니다.

* 에서 `getCompanyMembership`로 `companyArray` `membershipArray`변경되었습니다.

* in, `addUser`, `setCompanyMembership`and, `addCompanyMembership`changed `membershipArray` to `companyHandleArray`.

* 에서 `getCompanyMembership`로 `companyArray` `membershipArray`변경되었습니다.

* 에서 `getUserChars`이제 `includeInvalid` 선택 사항입니다.

**제거됨**

* 에서 `renameFiles` 제거되었습니다 `renameAsset`.

* Removed `getXMPPanelViewDefinition`.
* 제거됨 `searchAssetsByFulltext` 및 `searchAssetsBySimilarity`.

