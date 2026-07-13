---
description: 이미지 렌더링 소스 데이터 파일에는 비네팅 파일, 재질 파일(반복 가능한 텍스처 및 데칼에 대한 이미지, 캐비닛 및 창 커버링 스타일 파일) 및 ICC 프로파일이 포함됩니다.
solution: Experience Manager
title: Source 데이터
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: de2d8fa2-6793-49ba-b873-adf723369cce
TQID: 'https://experienceleague.adobe.com/lvrZxGOZbo6ORttqcBhCTuYPzbiD9xei5qkRwnapIh8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 258
ht-degree: 0%

---

# Source 데이터{#source-data}

이미지 렌더링 소스 데이터 파일에는 비네팅 파일, 재질 파일(반복 가능한 텍스처 및 데칼에 대한 이미지, 캐비닛 및 창 커버링 스타일 파일) 및 ICC 프로파일이 포함됩니다.

모든 소스 데이터 파일은 이미지 서버와 함께 제공되는 이미지 렌더링의 기본 코드 구성 요소에 액세스할 수 있어야 합니다.

재질 카탈로그가 포함된 경우 재질 카탈로그에 지정된 파일(`vignette::Path`, `catalog::Path` 또는 `icc::ProfilePath` 포함)은 렌더링 서버에서 다음과 같이 조회합니다.

* 경로가 절대적이면 그대로 사용됩니다.
* 상대 경로인 경우 앞에 `catalog::RootPath`(명명된 재질 카탈로그의)이 붙습니다.
* 경로가 절대적이면 이 경로가 사용됩니다. 그렇지 않으면 기본 카탈로그의 `default::RootPath` 접두사가 붙습니다.
* 경로가 절대적이면 이 경로가 사용됩니다. 그렇지 않으면 서버는 경로를 [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2)에 지정된 경로와 결합합니다.
* 이제 경로가 절대적이면 경로가 사용됩니다. 그렇지 않으면 [!DNL *[!DNL install_folder]*]에 대한 경로로 간주됩니다.

이미지 카탈로그가 포함되지 않은 경우 경로가 `default::RootPath`과(와) 결합된 다음 위와 같이 처리됩니다.

원본 데이터 파일의 실제 위치는 일반적으로 [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2)(으)로 지정됩니다. 소스 데이터 파일이 여러 파일 시스템에 분산되도록 여러 값을 지정할 수 있습니다. 렌더링 서버는 데이터 파일이 발견될 때까지 지정된 순서대로 각 경로를 시도합니다.

모든 종류의 새 데이터 파일은 서버를 중지하지 않고 언제든지 추가할 수 있습니다.

