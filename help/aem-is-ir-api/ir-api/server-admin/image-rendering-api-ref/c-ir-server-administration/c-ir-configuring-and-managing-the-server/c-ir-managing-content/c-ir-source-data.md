---
description: 이미지 렌더링 소스 데이터 파일에는 비네팅 파일, 재질 파일(반복 가능한 텍스처 및 데칼에 대한 이미지, 캐비닛 및 창 커버링 스타일 파일) 및 ICC 프로파일이 포함됩니다.
solution: Experience Manager
title: 소스 데이터
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: de2d8fa2-6793-49ba-b873-adf723369cce
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 0%

---

# 소스 데이터{#source-data}

이미지 렌더링 소스 데이터 파일에는 비네팅 파일, 재질 파일(반복 가능한 텍스처 및 데칼에 대한 이미지, 캐비닛 및 창 커버링 스타일 파일) 및 ICC 프로파일이 포함됩니다.

모든 소스 데이터 파일은 이미지 서버와 함께 제공되는 이미지 렌더링의 기본 코드 구성 요소에 액세스할 수 있어야 합니다.

재질 카탈로그가 포함된 경우 재질 카탈로그에 지정된 파일(포함) `vignette::Path`, `catalog::Path`, 또는 `icc::ProfilePath`)는 다음과 같이 렌더링 서버에서 조회합니다.

* 경로가 절대적이면 그대로 사용됩니다.
* 경로가 상대적인 경우 접두사가 붙습니다. `catalog::RootPath` (명명된 재질 카탈로그에서).
* 경로가 절대적이면 이 경로가 사용되고, 그렇지 않으면 이 접두사가 붙습니다. `default::RootPath` (기본 카탈로그에서).
* 경로가 절대적이면 이 경로가 사용됩니다. 그렇지 않으면 서버가 경로를 지정된 경로와 결합합니다. [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2).
* 이제 경로가 절대적이면 이 경로가 사용됩니다. 그렇지 않으면 [!DNL]에 대한 경로로 간주됩니다  *[!DNL install_folder]*].

이미지 카탈로그가 포함되지 않으면 경로가 와 결합됩니다. `default::RootPath` 그런 다음 위와 같이 처리됩니다.

일반적으로 소스 데이터 파일의 물리적 위치는 [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2). 소스 데이터 파일이 여러 파일 시스템에 분산되도록 여러 값을 지정할 수 있습니다. 렌더링 서버는 데이터 파일을 찾을 때까지 지정된 순서대로 각 경로를 시도합니다.

모든 종류의 새 데이터 파일은 서버를 중지하지 않고 언제든지 추가할 수 있습니다.
