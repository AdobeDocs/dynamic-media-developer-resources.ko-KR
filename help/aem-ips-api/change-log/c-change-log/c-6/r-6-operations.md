---
description: IPS API 버전 6의 새 작업 방법 및 변경된 작업 방법에 대해 설명합니다.
seo-description: IPS API 버전 6의 새 작업 방법 및 변경된 작업 방법에 대해 설명합니다.
seo-title: 작업 새로 만들기 및 수정됨
solution: Experience Manager
title: 작업 새로 만들기 및 수정됨
topic: Scene7 Image Production System API
uuid: e36f0d5c-0170-4a65-9347-c7fd3538726b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 2%

---


# 작업:새로 만들기 및 수정됨{#operations-new-and-modified}

IPS API 버전 6의 새 작업 방법 및 변경된 작업 방법에 대해 설명합니다.

구문

## 새 작업 {#section-088502a0746945f28a5ea100cd655bc6}

* `batchGetAssetPublishContexts`
* `getPublishContexts`
* `moveFolder`
* `setAssetsContexState`
* `updateAssetSet`
* `updateImageSet`

## 수정한 작업 {#section-f4e8755527444266ae806e3f4c851ae6}

**추가됨**

* 다음 항목에 `isHidden` 및 `initialTagValue`이(가) 추가되었습니다.

   * `saveMetadataField`
   * ` `updateMetadataField&quot;
   * `createMetadataField`

* 다음에 `thumbAssetHandle`을(를) 추가했습니다.

   * `createImageSet`
   * `createAssetSet`

   다음에 `companyHandle`을(를) 추가했습니다.

   * `getViewerConfigSettings`
   * `setViewerConfigSettings`
   * `updateViewerConfigSettings`
   * `getSearchStrings`

   다음에 `contextHandle`을(를) 추가했습니다.

   * `getImageServingPublishSettings`
   * `getImageRenderingPublishSettings`
   * `setImageServingPublishSettings`
   * `setImageRenderingPublishSettings`



* includeInactive가 다음에 추가되었습니다.

   * `getUsers`.
   * `getUserChars`.

* `permissionArray`을(를) `createPropertySet`에 추가했습니다.

* `exportJob`을(를) `submitJob`에 추가했습니다.

**변경**

* `addUser` 및 `setUser`에서 `role`을(를) `defaultRole`(으)로 변경했습니다.

* `getCompanyMembers`에서 `userArray`을(를) `memberArray`(으)로 변경했습니다.

* `getCompanyMembership`에서 `companyArray`을(를) `membershipArray`(으)로 변경했습니다.

* `addUser`, `setCompanyMembership` 및 `addCompanyMembership`에서 `membershipArray`을(를) `companyHandleArray`로 변경했습니다.

* `getCompanyMembership`에서 `companyArray`을(를) `membershipArray`(으)로 변경했습니다.

* `getUserChars`에서 `includeInvalid`은 이제 선택 사항입니다.

**제거됨**

* `renameAsset`에서 `renameFiles`을(를) 제거했습니다.

* `getXMPPanelViewDefinition`이(가) 제거되었습니다.
* `searchAssetsByFulltext` 및 `searchAssetsBySimilarity`이(가) 제거되었습니다.

