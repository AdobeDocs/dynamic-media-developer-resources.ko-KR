---
description: 캐시 항목은 CacheValidationPolicy 속성을 사용하여 선택한 대로 카탈로그 기반 또는 만료 기반 캐시 유효성 검사를 사용하여 자동으로 새로 고쳐집니다(기본값.ini 또는 특정 이미지 카탈로그의 .ini 파일).
seo-description: 캐시 항목은 CacheValidationPolicy 속성을 사용하여 선택한 대로 카탈로그 기반 또는 만료 기반 캐시 유효성 검사를 사용하여 자동으로 새로 고쳐집니다(기본값.ini 또는 특정 이미지 카탈로그의 .ini 파일).
seo-title: 응답 캐시 유효성 검사
solution: Experience Manager
title: 응답 캐시 유효성 검사
topic: Scene7 Image Serving - Image Rendering API
uuid: d1aad5ae-f0fa-489b-a48b-b0ac8c8f43bb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 응답 캐시 유효성 검사{#response-cache-validation}

캐시 항목은 다음과 같이 카탈로그 기반 또는 만료 기반 캐시 유효성 검사를 사용하여 자동으로 새로 고쳐집니다. 속성::CacheValidationPolicy(기본값.ini 또는 특정 이미지 카탈로그의 .ini 파일)와 함께 선택됩니다.

카탈로그 기반 유효성 검사 시 캐시 항목이 캐시 항목을 만든 `catalog::LastModified` 시간보다 최근 경우 `attribute::LastModified`또는 [!DNL catalog.ini] 파일의 파일 수정 시간이 오래된 것으로 간주됩니다.

만료 기반 유효성 검사를 통해 캐시 항목은 최근 유효성 검사 이후 5분 후에 만료됩니다. 두 경우 모두, 서버는 요청을 만드는 데 관련된 모든 이미지 파일의 파일 날짜를 확인하여 부실 캐시 항목을 검증합니다. 파일 날짜가 변경되지 않으면 캐시 항목의 타임스탬프가 업데이트되고 캐시된 날짜가 유효한 것으로 간주됩니다.

이미지 카탈로그에 등록된 대부분의 이미지가 포함된 일반적인 애플리케이션의 경우 카탈로그 기반 유효성 검사를 통해 성능을 활용할 수 있습니다. 이미지 카탈로그가 포함되지 않은 응용 프로그램은 만료 기반 캐시 유효성 검사를 사용해야 합니다. 이를 실현하는 한 가지 방법은 `attribute::cacheValidationPolicy=0` 인 [!DNL default.ini]및 모든 특정 이미지 카탈로그 파일을 설정하는 `1` 것입니다.

캐시 항목은 유효하지 않게 되고, 요청과 관련된 카탈로그 항목이 회신 이미지를 변경할 때 다시 생성됩니다. 예를 들어, `catalog::Modifier` 변경 내용이 포함되어 있습니다.

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>Scene7 피라미드 TIFF(PTIFF) 이미지는 유효성 검사를 위해 파일 헤더에서 파일 날짜를 내부적으로 유지합니다. 파일 시스템에서 유지 관리하는 파일 수정 시간은 PTIFF가 아닌 파일이 변경되었는지 확인하는 데 사용됩니다.

캐시 유효성 검사 프로세스에는 이미지 파일만 포함됩니다. 글꼴 파일이나 ICC 프로필 파일을 변경해도 캐시 항목이 자동으로 무효화되지 않습니다.
