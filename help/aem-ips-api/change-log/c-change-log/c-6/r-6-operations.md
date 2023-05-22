---
description: IPS API 버전 6에 대한 새로운 작업 및 변경된 작업 방법을 설명합니다.
solution: Experience Manager
title: 새 작업 및 수정된 작업
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fc7af77e-17fc-453a-8949-78c9c5c33b34
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 2%

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

* 추가됨 `isHidden` 및 `initialTagValue` 끝:

   * `saveMetadataField`
   * ` `updateMetadataField&quot;
   * `createMetadataField`

* 추가됨 `thumbAssetHandle` 끝:

   * `createImageSet`
   * `createAssetSet`

   추가됨 `companyHandle` 끝:

   * `getViewerConfigSettings`
   * `setViewerConfigSettings`
   * `updateViewerConfigSettings`
   * `getSearchStrings`

   추가됨 `contextHandle` 끝:

   * `getImageServingPublishSettings`
   * `getImageRenderingPublishSettings`
   * `setImageServingPublishSettings`
   * `setImageRenderingPublishSettings`



* includeInactive가 다음에 추가됨:

   * `getUsers`.
   * `getUserChars`.

* 추가됨 `permissionArray` 끝 `createPropertySet`.

* 추가됨 `exportJob` 끝 `submitJob`.

**변경**

* 위치 `addUser` 및 `setUser`, 변경됨 `role` 끝 `defaultRole`.

* 위치 `getCompanyMembers`, 변경됨 `userArray` 끝 `memberArray`.

* 위치 `getCompanyMembership`, 변경됨 `companyArray` 끝 `membershipArray`.

* 위치 `addUser`, `setCompanyMembership`, 및 `addCompanyMembership`, 변경됨 `membershipArray` 끝 `companyHandleArray`.

* 위치 `getCompanyMembership`, 변경됨 `companyArray` 끝 `membershipArray`.

* 위치 `getUserChars`, `includeInvalid` 는 이제 선택 사항입니다.

**제거됨**

* 제거됨 `renameFiles` 출처: `renameAsset`.

* 제거됨 `getXMPPanelViewDefinition`.
* 제거됨 `searchAssetsByFulltext` 및 `searchAssetsBySimilarity`.
