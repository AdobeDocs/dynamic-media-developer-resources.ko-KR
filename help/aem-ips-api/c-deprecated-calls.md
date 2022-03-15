---
title: 더 이상 사용되지 않는 호출
description: 이미지 프로덕션 시스템 API 호출과 Dynamic Media에서 더 이상 사용되지 않거나 지원되지 않는 관련 매개 변수
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f6711780-9a96-4a61-9066-8d83316758c3
source-git-commit: 25d9de1d9ba727e72c031ab22c47bd2be5c11050
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 0%

---

# 더 이상 사용되지 않는 호출{#deprecated-calls}

이미지 프로덕션 시스템 API 호출 및 더 이상 사용되지 않는 관련 매개 변수

## 더 이상 사용되지 않는 호출 {#topic-654c0466e6434fe4a95953322255b08c}

이미지 프로덕션 시스템 API 호출 및 Dynamic Media에서 더 이상 사용되지 않는 관련 매개 변수

* `ExcludeMasterVideoFromAVS` - 다음에서 사용 안 함 [데이터 유형](/help/aem-ips-api/types/c-data-types/c-data-types.md). 이 매개 변수는 응용 비디오 세트에서 기본 비디오를 제외했습니다.
   >[!IMPORTANT]
   >
   >Adobe은 2022년 9월 1일에 이 매개 변수에 대한 지원을 종료합니다. 참조 - [ExcludeMasterVideoFromAVS](/help/aem-ips-api/types/c-data-types/r-exclude-master-video-from-avs.md).

* `addMediaPortalEvent` - 다음에서 사용 안 함 [작업](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). 이 매개 변수를 사용하면 IPS에 Media Portal 이벤트를 추가할 수 있습니다.
* `getMediaPortalEvent` - 다음에서 사용 안 함 [작업](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). 이 매개 변수를 사용하면 지정된 기준과 일치하는 미디어 포털 이벤트를 가져올 수 있습니다.
* `getCdnCacheInvalidationStatus` - 다음에서 사용 안 함 [작업](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). 이 매개 변수는 이제 `cdnCacheInvalidation` 매개 변수가 캐시를 거의 즉시 무효화합니다(~5초). 따라서 무효화 상태에 대한 폴링이 더 이상 필요하지 않습니다.
