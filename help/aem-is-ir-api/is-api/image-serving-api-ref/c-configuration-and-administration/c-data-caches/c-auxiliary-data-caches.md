---
description: 중첩/포함된 요청에서 cache=on 을 지정하여 중첩/포함된 이미지 제공 및 이미지 렌더링 요청으로 생성된 중간 이미지 데이터를 캐시할 수 있습니다. 이 데이터는 응답 데이터 캐시에 고유한 형식으로 저장됩니다.
solution: Experience Manager
title: 보조 데이터 캐시
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 39906c86-fd9e-4961-a8ba-2ac44c4214a2
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 0%

---

# 보조 데이터 캐시{#auxiliary-data-caches}

중첩/포함된 요청에서 cache=on 을 지정하여 중첩/포함된 이미지 제공 및 이미지 렌더링 요청으로 생성된 중간 이미지 데이터를 캐시할 수 있습니다. 이 데이터는 응답 데이터 캐시에 고유한 형식으로 저장됩니다.

외부 HTTP 서버에서 가져온 이미지도 응답 데이터 캐시에 저장됩니다. 이러한 이미지는 캐시 항목이 생성되기 전에 유효성 검사 유틸리티를 사용하여 자동으로 검증됩니다.

Platform Server는 효율적인 액세스를 위해 이미지 카탈로그 데이터를 컴파일합니다. 이 데이터는 `CS::CatalogCacheFolder`에 저장됩니다.
