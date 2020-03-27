---
description: 베타 WSDL 파섹
seo-description: 베타 WSDL 파섹
seo-title: 제한된 사용
solution: Experience Manager
title: 제한된 사용
topic: Scene7 Image Production System API
uuid: 76a423e5-ff7d-44a3-aba4-af258ea55256
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 제한된 사용{#restricted-use}

베타 WSDL 파섹

이러한 작업 및 유형은 이후 시스템 업데이트를 비활성화, 변경 또는 비활성화할 수 있습니다.

**새 유형**

* AssetPublishContexts
* AssetPublishContextsArray
* CompanyMetadataInfo
* CompanyMetadataInfoArray
* CreateVideoSitemapJob
* PublishContext
* PublishContextArray
* SearchFilter
* LongArray

**새 작업**

* applyMetadataTemplate
* batch 파섹
* createCompanyMetadata
* deleteCompanyMetadata
* getCompanyMetadata
* getPublishContexts
* listCompanyMetadata
* removeMask
* removePropertySetPermissions
* searchAssetsBySimilarity
* searchAssetsByFulltext
* setAssetPublishState
* setPropertySetPermissions
* updateAssetSet
* updateCompanyMetadata
* updateImageSet
* updatePropertySetPermissions

**수정된 유형**

* 유형을 `ActiveJob` 포함하도록 `createVideoSitemapJob` 변경됨

* 유형을 `ScheduledJob` 포함하도록 `createVideoSitemapJob` 변경됨

* 선택 `ImageServingPublishJob` 사항을 포함하도록 변경됨 `contextHandle`

* 선택 `ImageRenderingPublishJob` 사항을 포함하도록 변경됨 `contextHandle`

* 선택 `MetadataField` 사항을 포함하도록 변경됨 `initialTagField`

* 포함 및 선택적 매개 변수로 `MetadataCondition` `caseSensitive` 변경

* 옵션을 `PropertySet` 포함하도록 `PermissionArray` 변경했습니다. `permissions`

* 선택적 매개 변수 `UploadDirectoryJob` 및 `xmpKeywords``xmpTemplateId` `xmpTemplateOverride` 매개 변수를 포함하도록 변경했습니다.

* 선택 `VideoPublishJob` 사항을 포함하도록 변경됨 `contextHandle`

**수정된 작업**

* 선택 `createAssetSet` 사항을 포함하도록 변경됨 `thumbAssetHandle`

* 선택 `createImageSet` 사항을 포함하도록 변경됨 `thumbAssetHandle`

* 선택적 매개 변수를 `createMetadataField` 포함하도록 `initialTagValue` 변경됨

* 옵션을 `createPropertySet` 포함하도록 `PermissionUpdateArray` 변경했습니다. `permissionArray`

* 선택적 매개 변수를 `getImageServingPublishSettings` 포함하도록 `contextHandle` 변경됨

* 선택적 매개 변수를 `getImageRenderingPublishSettings` 포함하도록 `contextHandle` 변경됨

* 일련의 선택적 매개 변수를 포함하도록 `searchAssetsByFullText` 변경되었습니다.

   * `SearchFilter` as `filters` parameter

   * `sortBy`
   * `sortDirection`

* 일련의 선택적 매개 변수를 포함하도록 `searchAssetsByMetadata` 변경되었습니다.

   * `SearchFilter` as `filters` parameter

   * `sortBy`
   * `sortDirection`
   * `haystackSearch` 7개의 매개 변수 순서

* 옵션을 `setAssetPublishState` 포함하도록 `HandleArray` 변경했습니다. `contextHandleArray`

* 선택적 매개 변수를 `setImageServingPublishSettings` 포함하도록 `contextHandle` 변경됨

* 선택적 `setImageRenderingPublishSettings` 매개 변수를 `contextHandle`포함하도록 변경했습니다.

* 선택적 작업 유형을 `submitJob` 포함하도록 `createVideoSitemap` 변경됨

