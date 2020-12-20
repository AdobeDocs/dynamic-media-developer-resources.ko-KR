---
description: 베타 WSDL에서 사용할 수 있는 이러한 새로운 작업 또는 수정된 작업 및 데이터 유형은 Scene7 개발 응용 프로그램 외부에서 사용되지 않습니다.
seo-description: 베타 WSDL에서 사용할 수 있는 이러한 새로운 작업 또는 수정된 작업 및 데이터 유형은 Scene7 개발 응용 프로그램 외부에서 사용되지 않습니다.
seo-title: 제한된 사용
solution: Experience Manager
title: 제한된 사용
topic: Scene7 Image Production System API
uuid: 76a423e5-ff7d-44a3-aba4-af258ea55256
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 0%

---


# 제한된 사용{#restricted-use}

베타 WSDL에서 사용할 수 있는 이러한 새로운 작업 또는 수정된 작업 및 데이터 유형은 Scene7 개발 응용 프로그램 외부에서 사용되지 않습니다.

이러한 작업 및 유형은 이후 시스템 업데이트를 비활성화, 변경 또는 사용하지 않을 수 있습니다.

**새 유형**

* AssetPublishContext
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
* batchGetAssetPublishContext
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

**수정된 형식**

* `ActiveJob`이(가) `createVideoSitemapJob` 유형을 포함하도록 변경되었습니다.

* `ScheduledJob`이(가) `createVideoSitemapJob` 유형을 포함하도록 변경되었습니다.

* 선택 사항 `contextHandle`을(를) 포함하도록 `ImageServingPublishJob`을(를) 변경했습니다.

* 선택 사항 `contextHandle`을(를) 포함하도록 `ImageRenderingPublishJob`을(를) 변경했습니다.

* 선택 사항 `initialTagField`을(를) 포함하도록 `MetadataField`을(를) 변경했습니다.

* `MetadataCondition`이(가) 포함 및 선택적 `caseSensitive` 매개 변수를 변경했습니다.

* `PropertySet`이(가) 옵션 `PermissionArray`을(를) `permissions`(으)로 포함하도록 변경되었습니다.

* 선택 사항 `xmpKeywords`, `xmpTemplateId` 및 `xmpTemplateOverride` 매개 변수를 포함하도록 `UploadDirectoryJob`이(가) 변경되었습니다.

* 선택 사항 `contextHandle`을(를) 포함하도록 `VideoPublishJob`을(를) 변경했습니다.

**수정된 작업**

* 선택 사항 `thumbAssetHandle`을(를) 포함하도록 `createAssetSet`을(를) 변경했습니다.

* 선택 사항 `thumbAssetHandle`을(를) 포함하도록 `createImageSet`을(를) 변경했습니다.

* 선택적 `initialTagValue` 매개 변수를 포함하도록 `createMetadataField`이(가) 변경되었습니다.

* `createPropertySet`이(가) 옵션 `PermissionUpdateArray`을(를) `permissionArray`(으)로 포함하도록 변경되었습니다.

* 선택적 `contextHandle` 매개 변수를 포함하도록 `getImageServingPublishSettings`이(가) 변경되었습니다.

* 선택적 `contextHandle` 매개 변수를 포함하도록 `getImageRenderingPublishSettings`이(가) 변경되었습니다.

* 다음과 같은 일련의 선택적 매개 변수를 포함하도록 `searchAssetsByFullText`이(가) 변경되었습니다.

   * `SearchFilter` as  `filters` parameter

   * `sortBy`
   * `sortDirection`

* 다음과 같은 일련의 선택적 매개 변수를 포함하도록 `searchAssetsByMetadata`이(가) 변경되었습니다.

   * `SearchFilter` as  `filters` parameter

   * `sortBy`
   * `sortDirection`
   * `haystackSearch` 7개의 매개 변수 순서

* `setAssetPublishState`이(가) 옵션 `HandleArray`을(를) `contextHandleArray`(으)로 포함하도록 변경되었습니다.

* 선택적 `contextHandle` 매개 변수를 포함하도록 `setImageServingPublishSettings`이(가) 변경되었습니다.

* 선택적 `contextHandle`매개 변수를 포함하도록 `setImageRenderingPublishSettings`이(가) 변경되었습니다.

* 선택적 `createVideoSitemap` 작업 유형을 포함하도록 `submitJob`이(가) 변경되었습니다.

