---
title: 더 이상 사용되지 않는 호출
description: 이미지 프로덕션 시스템 API 호출 및 Dynamic Media에서 더 이상 사용되지 않는 관련 매개 변수
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f6711780-9a96-4a61-9066-8d83316758c3
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 0%

---

# 더 이상 사용되지 않는 호출{#deprecated-calls}

이미지 프로덕션 시스템 API 호출 및 더 이상 사용되지 않는 관련 매개 변수

## 더 이상 사용되지 않는 호출 {#topic-654c0466e6434fe4a95953322255b08c}

이미지 프로덕션 시스템 API 호출 및 Dynamic Media에서 더 이상 사용되지 않는 관련 매개 변수

* `addMediaPortalEvent` - 작업에서 더 이상 사용되지 않습니다. 이 호출을 통해 IPS에 Media Portal 이벤트를 추가할 수 있습니다.
* `getMediaPortalEvent` - 작업에서 더 이상 사용되지 않습니다. 이 호출을 사용하면 지정된 기준과 일치하는 미디어 포털 이벤트를 가져올 수 있습니다.
* `getCdnCacheInvalidationStatus` - 작업에서 더 이상 사용되지 않습니다. 이제 `cdnCacheInvalidation` API가 캐시를 거의 즉시(~5초) 무효화하므로 이 API는 더 이상 사용되지 않습니다. 따라서 무효화 상태에 대한 폴링이 더 이상 필요하지 않습니다.
