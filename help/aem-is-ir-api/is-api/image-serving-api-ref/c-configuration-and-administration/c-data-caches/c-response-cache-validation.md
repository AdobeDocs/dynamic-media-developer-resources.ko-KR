---
description: CacheValidationPolicy 속성을 사용하여 선택한 대로, CacheValidationPolicy 속성을 사용하여(default.ini 또는 특정 이미지 카탈로그의 .ini 파일)를 사용하여 캐시 항목은 자동으로 새로 고쳐집니다.
seo-description: CacheValidationPolicy 속성을 사용하여 선택한 대로, CacheValidationPolicy 속성을 사용하여(default.ini 또는 특정 이미지 카탈로그의 .ini 파일)를 사용하여 캐시 항목은 자동으로 새로 고쳐집니다.
seo-title: 응답 캐시 유효성 검사
solution: Experience Manager
title: 응답 캐시 유효성 검사
topic: Scene7 Image Serving - Image Rendering API
uuid: d1aad5ae-f0fa-489b-a48b-b0ac8c8f43bb
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 0%

---


# 응답 캐시 유효성 검사{#response-cache-validation}

Cache 항목은 다음과 같이 속성::CacheValidationPolicy(default.ini 또는 특정 이미지 카탈로그의 .ini 파일)와 함께 선택한 대로 카탈로그 기반 또는 만료 기반 캐시 유효성 검사를 사용하여 자동으로 새로 고쳐집니다.

카탈로그 기반 유효성 검사 시 기존 캐시 항목 `catalog::LastModified` 은 캐시 항목이 생성된 시간보다 더 최근 `attribute::LastModified`에 있는 경우 [!DNL catalog.ini] (또는 파일의 파일 수정 시간)이 오래된 것으로 간주됩니다.

만료 기반 유효성 검사 기능을 사용하면 최근 유효성 검사 이후 5분 후에 캐시 항목이 오래된 상태가 됩니다. 두 경우 모두에서 서버는 요청을 만드는 데 관련된 모든 이미지 파일의 파일 날짜를 확인하여 부실 캐시 항목을 검증합니다. 파일 날짜가 변경되지 않으면 캐시 항목의 타임스탬프가 업데이트되고 캐시된 날짜가 유효한 것으로 간주됩니다.

일반적으로 이미지 카탈로그에 등록된 이미지가 주로 포함된 애플리케이션의 경우 카탈로그 기반 유효성 검사가 성능 이점을 제공합니다. 이미지 카탈로그가 포함되지 않은 응용 프로그램은 만료 기반 캐시 유효성 검사를 사용해야 합니다. 이를 실현하는 한 가지 방법은 `attribute::cacheValidationPolicy=0` 모든 특정 이미지 카탈로그 파일 [!DNL default.ini]에 설정 `1` 및 설정하는 것입니다.

캐시 항목은 유효하지 않게 되고, 요청과 관련된 카탈로그 항목이 회신 이미지를 변경하는 방법으로 변경될 때 다시 생성됩니다. 예를 들어 변경 내용이 포함되어 `catalog::Modifier` 있습니다.

>[!NOTE]
>
>Scene7 피라미드 TIFF(PTIFF) 이미지는 파일 헤더의 파일 날짜를 유효성 검사 목적으로 내부적으로 유지합니다. 파일 시스템에서 유지 관리하는 파일 수정 시간은 PTIFF가 아닌 파일이 변경되었는지 확인하는 데 사용됩니다.

이미지 파일만 캐시 유효성 검사 프로세스에 참여할 수 있습니다. 글꼴 파일 또는 ICC 프로필 파일을 변경해도 캐시 항목의 자동 무효화는 발생하지 않습니다.
