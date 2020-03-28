---
description: 이미지 렌더링 소스 데이터 파일에는 비네팅 파일, 재료 파일(반복 가능한 텍스처 및 디캘용 이미지, 캐비닛 및 창 적용 스타일 파일), ICC 프로파일이 포함됩니다.
seo-description: 이미지 렌더링 소스 데이터 파일에는 비네팅 파일, 재료 파일(반복 가능한 텍스처 및 디캘용 이미지, 캐비닛 및 창 적용 스타일 파일), ICC 프로파일이 포함됩니다.
seo-title: 소스 데이터
solution: Experience Manager
title: 소스 데이터
topic: Scene7 Image Serving - Image Rendering API
uuid: 76c6419c-613e-4eff-b30f-9fea2a7daf5b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 소스 데이터{#source-data}

이미지 렌더링 소스 데이터 파일에는 비네팅 파일, 재료 파일(반복 가능한 텍스처 및 디캘용 이미지, 캐비닛 및 창 적용 스타일 파일), ICC 프로파일이 포함됩니다.

모든 소스 데이터 파일은 이미지 렌더링의 기본 코드 구성 요소(이미지 서버와 함께 위치)에서 액세스할 수 있어야 합니다.

자재 카탈로그가 관련된 경우, 재료 카탈로그에 지정된 파일(사용 `vignette::Path`, `catalog::Path`또는 `icc::ProfilePath`사용)이 다음과 같이 Render Server에서 조회합니다.

* 경로가 절대이면 있는 그대로 사용됩니다.
* 경로가 상대적이면 `catalog::RootPath` (명명된 재료 카탈로그에서) 접두사가 붙습니다.
* 경로가 절대이면 사용됩니다.그렇지 않으면 `default::RootPath` (기본 카탈로그에서) 접두사가 붙습니다.
* 경로가 절대이면 사용됩니다.그렇지 않으면 서버가 [ir.resourceRootPaths에 지정된 경로와 결합합니다](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2).
* 경로가 이제 절대이면 사용됩니다.그렇지 않으면 [!DNL *[!DNL install_folder]*]에 상대적이라고 가정합니다.

관련된 이미지 카탈로그가 없는 경우 경로는 과 결합된 `default::RootPath` 다음 위와 같이 처리됩니다.

소스 데이터 파일의 실제 위치는 일반적으로 [ir.resourceRootPaths로 지정됩니다](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2). 여러 값을 지정하여 여러 파일 시스템에 소스 데이터 파일을 배포할 수 있습니다. Render Server는 데이터 파일을 찾을 때까지 지정된 순서대로 각 경로를 시도합니다.

서버를 중지하지 않고도 언제든지 새로운 데이터 파일을 추가할 수 있습니다.
