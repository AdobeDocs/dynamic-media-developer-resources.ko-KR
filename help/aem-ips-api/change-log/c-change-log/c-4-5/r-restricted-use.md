---
description: Beta WSDL에서 사용할 수 있는 이러한 새로운 작업 또는 수정된 작업 및 데이터 유형은 Dynamic Media로 개발된 응용 프로그램 외부에서 사용할 수 없습니다.
solution: Experience Manager
title: 제한된 사용
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6602c5bc-9f75-4885-ae14-cab14e6afa5e
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# 제한된 사용{#restricted-use}

Beta WSDL에서 사용할 수 있는 이러한 새로운 작업 또는 수정된 작업 및 데이터 유형은 Dynamic Media로 개발된 응용 프로그램 외부에서 사용할 수 없습니다.

이러한 작업 및 유형은 후속 시스템 업데이트 시 비활성화, 변경 또는 사용 중단될 수 있습니다.

**새 형식**

* AssetPublishContext
* AssetPublishContextArray
* 회사 메타데이터 정보
* 회사 메타데이터 정보 배열
* CreateVideoSitemapJob
* 게시 컨텍스트
* PublishContextArray
* SearchFilter
* 긴 배열

**새 작업**

* applyMetadataTemplate
* batchGetAssetPublishContext
* createCompanyMetdata
* delete회사 메타데이터
* getCompanyMeta
* getPublishContexts
* listCompanyMeta
* removeMask
* removePropertySetPermissions
* searchAssetsBySimilarity
* searchAssetsByFulltext
* setAssetPublishState
* setPropertySetPermissions
* updateAsset
* updateCompanyMeta
* 이미지 집합 업데이트
* updatePropertySetPermissions

**수정된 형식**

* `ActiveJob` 형식을 포함하도록 `createVideoSitemapJob`을(를) 변경했습니다.

* `ScheduledJob` 형식을 포함하도록 `createVideoSitemapJob`을(를) 변경했습니다.

* 선택적 `ImageServingPublishJob`을(를) 포함하도록 `contextHandle`을(를) 변경했습니다.

* 선택적 `ImageRenderingPublishJob`을(를) 포함하도록 `contextHandle`을(를) 변경했습니다.

* 선택적 `MetadataField`을(를) 포함하도록 `initialTagField`을(를) 변경했습니다.

* 및 선택적 `MetadataCondition` 매개 변수를 포함하도록 `caseSensitive`을(를) 변경했습니다.

* 선택적 `PropertySet`을(를) `PermissionArray`(으)로 포함하도록 `permissions`을(를) 변경함

* 선택적 `UploadDirectoryJob`, `xmpKeywords` 및 `xmpTemplateId` 매개 변수를 포함하도록 `xmpTemplateOverride`을(를) 변경했습니다.

* 선택적 `VideoPublishJob`을(를) 포함하도록 `contextHandle`을(를) 변경했습니다.

**수정된 작업**

* 선택적 `createAssetSet`을(를) 포함하도록 `thumbAssetHandle`을(를) 변경했습니다.

* 선택적 `createImageSet`을(를) 포함하도록 `thumbAssetHandle`을(를) 변경했습니다.

* 선택적 `createMetadataField` 매개 변수를 포함하도록 `initialTagValue`을(를) 변경했습니다.

* 선택적 `createPropertySet`을(를) `PermissionUpdateArray`(으)로 포함하도록 `permissionArray`을(를) 변경함

* 선택적 `getImageServingPublishSettings` 매개 변수를 포함하도록 `contextHandle`을(를) 변경했습니다.

* 선택적 `getImageRenderingPublishSettings` 매개 변수를 포함하도록 `contextHandle`을(를) 변경했습니다.

* 일련의 선택적 매개 변수를 포함하도록 `searchAssetsByFullText`을(를) 변경했습니다.

   * `SearchFilter` 매개 변수로 `filters`

   * `sortBy`
   * `sortDirection`

* 일련의 선택적 매개 변수를 포함하도록 `searchAssetsByMetadata`을(를) 변경했습니다.

   * `SearchFilter` 매개 변수로 `filters`

   * `sortBy`
   * `sortDirection`
   * 7개 매개 변수의 `haystackSearch` 시퀀스

* 선택적 `setAssetPublishState`을(를) `HandleArray`(으)로 포함하도록 `contextHandleArray`을(를) 변경함

* 선택적 `setImageServingPublishSettings` 매개 변수를 포함하도록 `contextHandle`을(를) 변경했습니다.

* 선택적 `setImageRenderingPublishSettings` 매개 변수를 포함하도록 `contextHandle`을(를) 변경했습니다.

* 선택적 `submitJob` 작업 유형을 포함하도록 `createVideoSitemap`을(를) 변경했습니다.
