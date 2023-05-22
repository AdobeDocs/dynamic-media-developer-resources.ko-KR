---
description: Beta WSDL에서 사용할 수 있는 이러한 새로운 작업 또는 수정된 작업 및 데이터 유형은 Dynamic Media에서 개발한 애플리케이션 외부에서 사용할 수 없습니다.
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

Beta WSDL에서 사용할 수 있는 이러한 새로운 작업 또는 수정된 작업 및 데이터 유형은 Dynamic Media에서 개발한 애플리케이션 외부에서 사용할 수 없습니다.

이러한 작업 및 유형은 후속 시스템 업데이트 시 비활성화, 변경 또는 사용 중단될 수 있습니다.

**새 유형**

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

**수정된 유형**

* 변경됨 `ActiveJob` 포함 `createVideoSitemapJob` 유형

* 변경됨 `ScheduledJob` 포함 `createVideoSitemapJob` 유형

* 변경됨 `ImageServingPublishJob` 선택 사항을 포함하려면 `contextHandle`

* 변경됨 `ImageRenderingPublishJob` 선택 사항을 포함하려면 `contextHandle`

* 변경됨 `MetadataField` 선택 사항을 포함하려면 `initialTagField`

* 변경됨 `MetadataCondition` 및 옵션 포함 `caseSensitive` 매개 변수

* 변경됨 `PropertySet` 선택 사항을 포함하려면 `PermissionArray` 다음으로: `permissions`

* 변경됨 `UploadDirectoryJob` 옵션 포함 `xmpKeywords`, `xmpTemplateId` 및 `xmpTemplateOverride` 매개 변수

* 변경됨 `VideoPublishJob` 선택 사항을 포함하려면 `contextHandle`

**수정된 작업**

* 변경됨 `createAssetSet` 선택 사항을 포함하려면 `thumbAssetHandle`

* 변경됨 `createImageSet` 선택 사항을 포함하려면 `thumbAssetHandle`

* 변경됨 `createMetadataField` 선택 사항을 포함하려면 `initialTagValue` 매개 변수

* 변경됨 `createPropertySet` 선택 사항을 포함하려면 `PermissionUpdateArray` 다음으로: `permissionArray`

* 변경됨 `getImageServingPublishSettings` 선택 사항을 포함하려면 `contextHandle` 매개 변수

* 변경됨 `getImageRenderingPublishSettings` 선택 사항을 포함하려면 `contextHandle` 매개 변수

* 변경됨 `searchAssetsByFullText` 일련의 선택적 매개 변수를 포함하려면 다음을 수행합니다.

   * `SearchFilter` 다음으로: `filters` 매개 변수

   * `sortBy`
   * `sortDirection`

* 변경됨 `searchAssetsByMetadata` 일련의 선택적 매개 변수를 포함하려면 다음을 수행합니다.

   * `SearchFilter` 다음으로: `filters` 매개 변수

   * `sortBy`
   * `sortDirection`
   * `haystackSearch` 7개 매개 변수의 시퀀스

* 변경됨 `setAssetPublishState` 선택 사항을 포함하려면 `HandleArray` 다음으로: `contextHandleArray`

* 변경됨 `setImageServingPublishSettings` 선택 사항을 포함하려면 `contextHandle` 매개 변수

* 변경됨 `setImageRenderingPublishSettings` 선택 사항을 포함하려면 `contextHandle`매개 변수

* 변경됨 `submitJob` 선택 사항을 포함하려면 `createVideoSitemap` 작업 유형
