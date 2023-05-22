---
title: 더 이상 사용되지 않는 호출
description: 에서 더 이상 사용되지 않거나 지원되지 않는 이미지 프로덕션 시스템 API 호출 및 관련 매개 변수 [!DNL Dynamic Media].
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f6711780-9a96-4a61-9066-8d83316758c3
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---

# 더 이상 사용되지 않는 호출{#deprecated-calls}

이미지 프로덕션 시스템 API 호출 및 더 이상 사용되지 않는 관련 매개 변수입니다.

## 더 이상 사용되지 않는 호출 {#topic-654c0466e6434fe4a95953322255b08c}

에서 더 이상 사용되지 않는 이미지 프로덕션 시스템 API 호출 및 관련 매개 변수 [!DNL Dynamic Media].

* `ExcludeMasterVideoFromAVS` - 더 이상 사용되지 않음 [데이터 유형](/help/aem-ips-api/types/c-data-types/c-data-types.md). 이 매개 변수는 응용 비디오 세트에서 기본 비디오를 제외했습니다. <!-- Adobe is ending support for this parameter on September 1, 2022. -->
* `addMediaPortalEvent` - 더 이상 사용되지 않음 [작업](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). 이 매개 변수를 사용하면 Media Portal 이벤트를 IPS에 추가할 수 있습니다.
* `getMediaPortalEvent` - 더 이상 사용되지 않음 [작업](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). 이 매개 변수를 사용하면 지정된 기준과 일치하는 Media Portal 이벤트를 가져올 수 있습니다.
* `getCdnCacheInvalidationStatus` - 더 이상 사용되지 않음 [작업](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). 이 매개 변수는 이제 `cdnCacheInvalidation` 매개 변수가 캐시를 거의 즉시 무효화합니다(~5초). 따라서 무효화 상태에 대한 폴링은 더 이상 필요하지 않습니다.
