---
description: 중첩/임베드된 이미지 제공 및 이미지 렌더링 요청으로 생성된 중간 이미지 데이터는 중첩/임베드된 요청에서 cache=on을 지정하여 캐시할 수 있습니다. 이 데이터는 응답 데이터 캐시에 전용 형식으로 저장됩니다.
solution: Experience Manager
title: 보조 데이터 캐시
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 39906c86-fd9e-4961-a8ba-2ac44c4214a2
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---

# 보조 데이터 캐시{#auxiliary-data-caches}

중첩/임베드된 이미지 제공 및 이미지 렌더링 요청으로 생성된 중간 이미지 데이터는 중첩/임베드된 요청에서 cache=on을 지정하여 캐시할 수 있습니다. 이 데이터는 응답 데이터 캐시에 전용 형식으로 저장됩니다.

외부 HTTP 서버에서 가져온 이미지도 응답 데이터 캐시에 저장됩니다. 이러한 이미지는 캐시 항목이 생성되기 전에 유효성 검사 유틸리티를 사용하여 자동으로 검증됩니다.

[!DNL Platform Server]은(는) 효율적인 액세스를 위해 이미지 카탈로그 데이터를 컴파일합니다. 이 데이터는 `CS::CatalogCacheFolder`에 저장됩니다.
