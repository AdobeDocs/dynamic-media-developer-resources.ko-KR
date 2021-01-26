---
description: 캐시 항목은 CacheValidationPolicy 속성(default.ini 또는 특정 이미지 카탈로그의 .ini 파일에서)으로 선택한 대로 카탈로그 기반 또는 만료 기반 캐시 유효성 검사를 사용하여 자동으로 새로 고쳐집니다.
seo-description: 캐시 항목은 CacheValidationPolicy 속성(default.ini 또는 특정 이미지 카탈로그의 .ini 파일에서)으로 선택한 대로 카탈로그 기반 또는 만료 기반 캐시 유효성 검사를 사용하여 자동으로 새로 고쳐집니다.
seo-title: 응답 캐시 유효성 검사
solution: Experience Manager
title: 응답 캐시 유효성 검사
topic: Dynamic Media Image Serving - Image Rendering API
uuid: d1aad5ae-f0fa-489b-a48b-b0ac8c8f43bb
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 0%

---


# 응답 캐시 유효성 검사{#response-cache-validation}

캐시 항목은 다음과 같이 속성::CacheValidationPolicy(default.ini 또는 특정 이미지 카탈로그의 .ini 파일에서)로 선택된 대로 카탈로그 기반 또는 만료 기반 캐시 유효성 검사를 사용하여 자동으로 새로 고쳐집니다.

카탈로그 기반 유효성 검사를 사용할 경우, 기존 캐시 항목은 캐시 항목이 만들어진 시간보다 최근 `catalog::LastModified`(또는 `attribute::LastModified` 또는 [!DNL catalog.ini] 파일의 파일 수정 시간이 더 최신이면 오래된 것으로 간주됩니다.

만료 기반 유효성 검사를 사용하면 최근 유효성 검사 이후 5분 후에 캐시 항목이 오래된 상태로 됩니다. 두 경우 모두에서 서버는 요청을 만드는 데 관련된 모든 이미지 파일의 파일 날짜를 확인하여 부실 캐시 항목의 유효성을 검사합니다. 파일 날짜가 변경되지 않으면 캐시 항목의 타임스탬프가 업데이트되고 캐시된 날짜가 유효한 것으로 간주됩니다.

이미지 카탈로그에 대부분 등록된 이미지가 포함된 일반 애플리케이션의 경우 카탈로그 기반 유효성 검사가 성능 이점을 제공합니다. 이미지 카탈로그가 포함되지 않은 응용 프로그램은 만료 기반 캐시 유효성 검사를 사용해야 합니다. 이를 실현하는 한 가지 방법은 [!DNL default.ini]에서 `attribute::cacheValidationPolicy=0`을 설정하고 모든 특정 이미지 카탈로그 파일에서 `1`로 설정하는 것입니다.

캐시 항목은 유효하지 않게 되고, 요청과 관련된 카탈로그 항목이 응답 이미지를 변경할 수 있는 방식으로 변경되면 다시 생성됩니다. 예를 들어 `catalog::Modifier`의 내용이 변경됩니다.

>[!NOTE]
>
>Dynamic Media 피라미드 TIFF(PTIFF) 이미지는 유효성 검사를 위해 파일 헤더의 내부 파일 날짜를 유지합니다. 파일 시스템에서 유지 관리하는 파일 수정 시간은 PTIFF가 아닌 파일이 변경되었는지 확인하는 데 사용됩니다.

이미지 파일만 캐시 유효성 검사 프로세스에 참여할 수 있습니다. 글꼴 파일 또는 ICC 프로필 파일을 변경하면 캐시 항목이 자동으로 무효화되지 않습니다.
