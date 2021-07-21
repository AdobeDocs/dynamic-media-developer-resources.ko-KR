---
description: 이미지 렌더링 소스 데이터 파일에는 비네팅 파일, 재료 파일(반복 가능한 텍스처 및 디캘용 이미지, 스타일 파일을 덮는 캐비닛 및 창)과 ICC 프로필이 포함됩니다.
solution: Experience Manager
title: 소스 데이터
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: de2d8fa2-6793-49ba-b873-adf723369cce
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# 소스 데이터{#source-data}

이미지 렌더링 소스 데이터 파일에는 비네팅 파일, 재료 파일(반복 가능한 텍스처 및 디캘용 이미지, 스타일 파일을 덮는 캐비닛 및 창)과 ICC 프로필이 포함됩니다.

모든 소스 데이터 파일은 이미지 렌더링(이미지 서버와 함께 있음)의 기본 코드 구성 요소에 액세스할 수 있어야 합니다.

재료 카탈로그가 포함되어 있으면 재료 카탈로그에 지정된 파일(`vignette::Path`, `catalog::Path` 또는 `icc::ProfilePath` 포함)은 다음과 같이 Render Server에서 조회합니다.

* 경로가 절대이면 그대로 사용됩니다.
* 경로가 상대적이면 `catalog::RootPath` 접두사가 붙습니다(명명된 재료 카탈로그에서).
* 경로가 절대이면 사용됩니다. 그렇지 않으면 `default::RootPath` 접두사가 붙습니다(기본 카탈로그에서).
* 경로가 절대이면 사용됩니다. 그렇지 않으면 서버가 [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2)에 지정된 경로와 결합합니다.
* 이제 경로가 절대이면 사용됩니다. 그렇지 않으면 [!DNL *[!DNL install_folder]*]에 상대적이라고 가정합니다.

이미지 카탈로그가 포함되지 않으면 경로가 `default::RootPath`과 결합되어 위와 같이 처리됩니다.

소스 데이터 파일의 실제 위치는 일반적으로 [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2)로 지정됩니다. 여러 파일 시스템에 소스 데이터 파일을 배포할 수 있도록 여러 값을 지정할 수 있습니다. Render Server는 데이터 파일이 발견될 때까지 지정된 순서대로 각 경로를 시도합니다.

서버를 중지하지 않고도 언제든지 모든 종류의 새 데이터 파일을 추가할 수 있습니다.
