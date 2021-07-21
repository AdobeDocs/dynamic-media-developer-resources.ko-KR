---
description: 재료 카탈로그는 많은 이미지 렌더링 구성 설정을 제공합니다.
solution: Experience Manager
title: 재료 카탈로그
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c0b030b7-bcfb-4e6d-b74a-4533bdb801bf
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 0%

---

# 재료 카탈로그{#material-catalogs}

재료 카탈로그는 많은 이미지 렌더링 구성 설정을 제공합니다.

재료 카탈로그는 요청에 사용된 비네트와 재료 ID를 실제 파일 경로에 매핑하고, 재료와 관련된 모든 메타데이터를 저장하고, 템플릿에 대한 컨테이너를 제공할 수 있습니다. ICC 프로필과 명령 매크로를 추적합니다.

자료 카탈로그는 이미지 렌더링(Platform Server와 함께 있음)의 Java 구성 요소에서만 액세스할 수 있습니다. 카탈로그 특성 파일에는 [!DNL .ini] 접미사가 있어야 하며 등록된 카탈로그 폴더([ir.catalogRootPath](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-catalog-folder.md#concept-1c1d308112054bb99e3895c3fb8ca5f7))에 배치되어야 합니다. 기본 자료 카탈로그( [!DNL default.ini])는 항상 있어야 하며 이미지 제공 기능의 올바른 수행을 위해 모든 속성을 채워야 합니다.
