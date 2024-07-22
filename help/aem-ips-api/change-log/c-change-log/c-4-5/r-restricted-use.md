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

* `createVideoSitemapJob` 형식을 포함하도록 `ActiveJob`을(를) 변경했습니다.

* `createVideoSitemapJob` 형식을 포함하도록 `ScheduledJob`을(를) 변경했습니다.

* 선택적 `contextHandle`을(를) 포함하도록 `ImageServingPublishJob`을(를) 변경했습니다.

* 선택적 `contextHandle`을(를) 포함하도록 `ImageRenderingPublishJob`을(를) 변경했습니다.

* 선택적 `initialTagField`을(를) 포함하도록 `MetadataField`을(를) 변경했습니다.

* 및 선택적 `caseSensitive` 매개 변수를 포함하도록 `MetadataCondition`을(를) 변경했습니다.

* 선택적 `PermissionArray`을(를) `permissions`(으)로 포함하도록 `PropertySet`을(를) 변경함

* 선택적 `xmpKeywords`, `xmpTemplateId` 및 `xmpTemplateOverride` 매개 변수를 포함하도록 `UploadDirectoryJob`을(를) 변경했습니다.

* 선택적 `contextHandle`을(를) 포함하도록 `VideoPublishJob`을(를) 변경했습니다.

**수정된 작업**

* 선택적 `thumbAssetHandle`을(를) 포함하도록 `createAssetSet`을(를) 변경했습니다.

* 선택적 `thumbAssetHandle`을(를) 포함하도록 `createImageSet`을(를) 변경했습니다.

* 선택적 `initialTagValue` 매개 변수를 포함하도록 `createMetadataField`을(를) 변경했습니다.

* 선택적 `PermissionUpdateArray`을(를) `permissionArray`(으)로 포함하도록 `createPropertySet`을(를) 변경함

* 선택적 `contextHandle` 매개 변수를 포함하도록 `getImageServingPublishSettings`을(를) 변경했습니다.

* 선택적 `contextHandle` 매개 변수를 포함하도록 `getImageRenderingPublishSettings`을(를) 변경했습니다.

* 일련의 선택적 매개 변수를 포함하도록 `searchAssetsByFullText`을(를) 변경했습니다.

   * `filters` 매개 변수로 `SearchFilter`

   * `sortBy`
   * `sortDirection`

* 일련의 선택적 매개 변수를 포함하도록 `searchAssetsByMetadata`을(를) 변경했습니다.

   * `filters` 매개 변수로 `SearchFilter`

   * `sortBy`
   * `sortDirection`
   * 7개 매개 변수의 `haystackSearch` 시퀀스

* 선택적 `HandleArray`을(를) `contextHandleArray`(으)로 포함하도록 `setAssetPublishState`을(를) 변경함

* 선택적 `contextHandle` 매개 변수를 포함하도록 `setImageServingPublishSettings`을(를) 변경했습니다.

* 선택적 `contextHandle` 매개 변수를 포함하도록 `setImageRenderingPublishSettings`을(를) 변경했습니다.

* 선택적 `createVideoSitemap` 작업 유형을 포함하도록 `submitJob`을(를) 변경했습니다.
