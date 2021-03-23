---
title: 사용되지 않는 호출
description: Dynamic Media에서 더 이상 사용되지 않는 이미지 프로덕션 시스템 API 호출 및 관련 매개 변수.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: 개발자,관리자
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 0%

---


# 사용되지 않는 호출{#deprecated-calls}

이미지 프로덕션 시스템 API 호출 및 더 이상 사용되지 않는 관련 매개 변수.

## 사용되지 않는 호출 {#topic-654c0466e6434fe4a95953322255b08c}

Dynamic Media에서 더 이상 사용되지 않는 이미지 프로덕션 시스템 API 호출 및 관련 매개 변수.

* `addMediaPortalEvent` - 작업에서 더 이상 사용되지 않습니다. 이 호출을 사용하여 IPS에 미디어 포털 이벤트를 추가할 수 있습니다.
* `getMediaPortalEvent` - 작업에서 더 이상 사용되지 않습니다. 이 호출을 사용하여 지정된 기준과 일치하는 미디어 포털 이벤트를 가져올 수 있습니다.
* `getCdnCacheInvalidationStatus` - 작업에서 더 이상 사용되지 않습니다. 이제 이 API는 `cdnCacheInvalidation` API가 거의 즉시 캐시를 무효화하므로 사용되지 않습니다(~5초). 따라서 무효화 상태에 대한 투표는 더 이상 필요하지 않습니다.

