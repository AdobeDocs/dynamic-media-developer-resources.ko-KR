---
description: 캐시 항목은 CacheValidationPolicy(default.ini 또는 특정 이미지 카탈로그의 .ini 파일)로 선택된 대로 카탈로그 기반 또는 만료 기반 캐시 유효성 검사를 사용하여 자동으로 새로 고쳐집니다.
solution: Experience Manager
title: 응답 캐시 유효성 검사
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: d2baa6e6-2700-450f-af1e-88b6d33d0e0c
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 0%

---

# 응답 캐시 유효성 검사{#response-cache-validation}

속성::CacheValidationPolicy(default.ini 또는 특정 이미지 카탈로그의 .ini 파일)로 선택된 경우, 캐시 항목은 카탈로그 기반 또는 만료 기반 캐시 유효성 검사를 사용하여 자동으로 새로 고쳐집니다.

카탈로그 기반 유효성 검사를 사용하면 `catalog::LastModified`(또는 `attribute::LastModified` 또는 [!DNL catalog.ini] 파일의 파일 수정 시간)이 캐시 항목을 만든 시간보다 최신인 경우 기존 캐시 항목이 오래된 것으로 간주됩니다.

만료 기반 유효성 검사를 사용하면 가장 최근 유효성 검사 이후 5분 후에 캐시 항목이 부실 상태가 됩니다. 두 경우 모두, 서버는 요청 생성과 관련된 모든 이미지 파일의 파일 날짜를 확인하여 부실 캐시 항목을 확인합니다. 파일 날짜가 변경되지 않은 경우 캐시 항목의 타임스탬프가 업데이트되고 캐시된 날짜가 유효한 것으로 간주됩니다.

이미지 카탈로그에 등록된 이미지가 대부분인 일반적인 응용 프로그램의 경우 카탈로그 기반 유효성 검사를 통해 성능이 향상됩니다. 이미지 카탈로그가 포함되지 않은 응용 프로그램은 만료 기반 캐시 유효성 검사를 사용해야 합니다. 이를 위해 `attribute::cacheValidationPolicy=0`에서 [!DNL default.ini]을(를) 설정하고 모든 특정 이미지 카탈로그 파일에서 `1`을(를) 설정하는 방법이 있습니다.

요청에 포함된 카탈로그 항목이 응답 이미지를 변경시킬 수 있는 방식으로 변경되면 캐시 항목이 유효하지 않게 되고 재생성됩니다. 예를 들어 `catalog::Modifier`의 내용이 변경됩니다.

>[!NOTE]
>
>Dynamic Media 피라미드 TIFF(PTIFF) 이미지는 유효성 검사를 위해 파일 헤더에서 파일 날짜를 내부적으로 유지합니다. 파일 시스템에서 유지 관리되는 파일 수정 시간은 PTIFF가 아닌 파일이 변경되었는지 확인하는 데 사용됩니다.

이미지 파일만 캐시 유효성 검사 프로세스에 참여합니다. 글꼴 파일 또는 ICC 프로파일 파일을 변경해도 캐시 항목이 자동으로 무효화되지 않습니다.
