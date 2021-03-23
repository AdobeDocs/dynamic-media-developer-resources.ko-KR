---
description: 이미지 렌더링 소스 데이터 파일에는 비네팅 파일, 재질 파일(반복 가능한 텍스처 및 디캘용 이미지, 스타일 파일을 덮는 캐비닛 및 창 포함)과 ICC 프로필이 포함되어 있습니다.
seo-description: 이미지 렌더링 소스 데이터 파일에는 비네팅 파일, 재질 파일(반복 가능한 텍스처 및 디캘용 이미지, 스타일 파일을 덮는 캐비닛 및 창 포함)과 ICC 프로필이 포함되어 있습니다.
seo-title: 소스 데이터
solution: Experience Manager
title: 소스 데이터
uuid: 76c6419c-613e-4eff-b30f-9fea2a7daf5b
feature: Dynamic Media Classic,SDK/API
role: 개발자,관리자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---


# 소스 데이터{#source-data}

이미지 렌더링 소스 데이터 파일에는 비네팅 파일, 재질 파일(반복 가능한 텍스처 및 디캘용 이미지, 스타일 파일을 덮는 캐비닛 및 창 포함)과 ICC 프로필이 포함되어 있습니다.

이미지 렌더링의 기본 코드 구성 요소(이미지 서버와 함께 있음)에서 모든 소스 데이터 파일에 액세스할 수 있어야 합니다.

재료 카탈로그가 관련된 경우, `vignette::Path`, `catalog::Path` 또는 `icc::ProfilePath`와 함께 재료 카탈로그에 지정된 파일이 다음과 같이 렌더링 서버에서 조회합니다.

* 경로가 절대이면 그대로 사용됩니다.
* 경로가 상대적이면 `catalog::RootPath`(명명된 재료 카탈로그에서)이 접두사로 추가됩니다.
* 경로가 절대이면 사용됩니다.그렇지 않은 경우 `default::RootPath`(기본 카탈로그에서) 접두어가 붙습니다.
* 경로가 절대이면 사용됩니다.그렇지 않으면 서버가 [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2)에 지정된 경로와 결합합니다.
* 경로가 이제 절대적 경로인 경우 사용됩니다.그렇지 않으면 [!DNL *[!DNL install_folder]*]을(를) 기준으로 합니다.

관련된 이미지 카탈로그가 없는 경우 경로는 `default::RootPath`과 결합된 후 위와 같이 처리됩니다.

소스 데이터 파일의 실제 위치는 일반적으로 [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2)로 지정됩니다. 여러 파일 시스템에 소스 데이터 파일을 배포할 수 있도록 여러 값을 지정할 수 있습니다. 렌더링 서버는 데이터 파일을 찾을 때까지 지정된 순서대로 각 경로를 시도합니다.

서버를 중지하지 않고도 언제든지 모든 유형의 새 데이터 파일을 추가할 수 있습니다.
