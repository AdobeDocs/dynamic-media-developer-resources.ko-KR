---
description: 베타 WSDL에서 사용할 수 있는 이러한 새로운 작업 또는 수정된 작업 및 데이터 유형은 Dynamic Media 개발 응용 프로그램 외부에서 사용하지 않습니다.
solution: Experience Manager
title: 제한된 사용
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6602c5bc-9f75-4885-ae14-cab14e6afa5e
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 0%

---

# 제한된 사용{#restricted-use}

베타 WSDL에서 사용할 수 있는 이러한 새로운 작업 또는 수정된 작업 및 데이터 유형은 Dynamic Media 개발 응용 프로그램 외부에서 사용하지 않습니다.

이러한 작업 및 유형은 후속 시스템 업데이트를 사용하지 않거나 변경하거나 사용하지 않을 수 있습니다.

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
* batchGetAssetPublishContexts
* createCompanyMetadata
* deleteCompanyMetadata
* getCompanyMetadata
* getPublishContexts
* listCompanyMetadata
* removeMask
* removePropertySetPermissions
* searchAssetsBy유사성
* searchAssetsByFulltext
* setAssetPublishState
* setPropertySetPermissions
* updateAssetSet
* updateCompanyMetadata
* updateImageSet
* updatePropertySetPermissions

**수정된 유형**

* `ActiveJob`이(가) `createVideoSitemapJob` 유형을 포함하도록 변경됨

* `ScheduledJob`이(가) `createVideoSitemapJob` 유형을 포함하도록 변경됨

* `ImageServingPublishJob`이(가) 옵션 `contextHandle`을 포함하도록 변경되었습니다.

* `ImageRenderingPublishJob`이(가) 옵션 `contextHandle`을 포함하도록 변경되었습니다.

* `MetadataField`이(가) 옵션 `initialTagField`을 포함하도록 변경되었습니다.

* `MetadataCondition`이(가) 포함 및 선택적 `caseSensitive` 매개 변수로 변경되었습니다.

* `PropertySet`이(가) 옵션 `PermissionArray`을 `permissions`(으)로 포함하도록 변경되었습니다.

* `UploadDirectoryJob`이 선택적 `xmpKeywords`, `xmpTemplateId` 및 `xmpTemplateOverride` 매개 변수를 포함하도록 변경되었습니다.

* `VideoPublishJob`이(가) 옵션 `contextHandle`을 포함하도록 변경되었습니다.

**수정된 작업**

* `createAssetSet`이(가) 옵션 `thumbAssetHandle`을 포함하도록 변경되었습니다.

* `createImageSet`이(가) 옵션 `thumbAssetHandle`을 포함하도록 변경되었습니다.

* `createMetadataField`이(가) 선택적 `initialTagValue` 매개 변수를 포함하도록 변경되었습니다.

* `createPropertySet`이(가) 옵션 `PermissionUpdateArray`을 `permissionArray`(으)로 포함하도록 변경되었습니다.

* `getImageServingPublishSettings`이(가) 선택적 `contextHandle` 매개 변수를 포함하도록 변경되었습니다.

* `getImageRenderingPublishSettings`이(가) 선택적 `contextHandle` 매개 변수를 포함하도록 변경되었습니다.

* 일련의 선택적 매개 변수를 포함하도록 `searchAssetsByFullText`을 변경했습니다.

   * `SearchFilter` as  `filters` parameter

   * `sortBy`
   * `sortDirection`

* 일련의 선택적 매개 변수를 포함하도록 `searchAssetsByMetadata`을 변경했습니다.

   * `SearchFilter` as  `filters` parameter

   * `sortBy`
   * `sortDirection`
   * `haystackSearch` 7개의 매개변수 순서

* `setAssetPublishState`이(가) 옵션 `HandleArray`을 `contextHandleArray`(으)로 포함하도록 변경되었습니다.

* `setImageServingPublishSettings`이(가) 선택적 `contextHandle` 매개 변수를 포함하도록 변경되었습니다.

* `setImageRenderingPublishSettings`이(가) 선택적 `contextHandle`매개 변수를 포함하도록 변경되었습니다.

* 옵션 `createVideoSitemap` 작업 유형을 포함하도록 `submitJob`을 변경했습니다.
