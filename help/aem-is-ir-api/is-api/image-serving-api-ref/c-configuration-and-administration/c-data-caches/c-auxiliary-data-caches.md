---
description: 중첩/포함된 이미지 제공 및 이미지 렌더링 요청으로 생성된 중간 이미지 데이터는 중첩/포함된 요청에 cache=on을 지정하여 캐싱할 수 있습니다. 이 데이터는 응답 데이터 캐시에 전용 형식으로 저장됩니다.
seo-description: 중첩/포함된 이미지 제공 및 이미지 렌더링 요청으로 생성된 중간 이미지 데이터는 중첩/포함된 요청에 cache=on을 지정하여 캐싱할 수 있습니다. 이 데이터는 응답 데이터 캐시에 전용 형식으로 저장됩니다.
seo-title: 보조 데이터 캐시
solution: Experience Manager
title: 보조 데이터 캐시
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 10ce998e-e300-4d24-9d92-a8693dade327
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 0%

---


# 보조 데이터 캐시{#auxiliary-data-caches}

중첩/포함된 이미지 제공 및 이미지 렌더링 요청으로 생성된 중간 이미지 데이터는 중첩/포함된 요청에 cache=on을 지정하여 캐싱할 수 있습니다. 이 데이터는 응답 데이터 캐시에 전용 형식으로 저장됩니다.

외부 HTTP 서버에서 얻은 이미지는 응답 데이터 캐시에도 저장됩니다. 이러한 이미지는 캐시 항목이 생성되기 전에 검증 유틸리티를 사용하여 자동으로 검증됩니다.

Platform Server는 효율적인 액세스를 위해 이미지 카탈로그 데이터를 컴파일합니다. 이 데이터는 `CS::CatalogCacheFolder`에 저장됩니다.
