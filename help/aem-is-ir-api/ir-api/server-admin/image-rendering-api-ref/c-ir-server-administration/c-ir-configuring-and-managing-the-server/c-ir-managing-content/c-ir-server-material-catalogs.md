---
description: 재질 카탈로그는 많은 이미지 렌더링 구성 설정을 제공합니다.
solution: Experience Manager
title: 자료 카탈로그
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c0b030b7-bcfb-4e6d-b74a-4533bdb801bf
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---

# 자료 카탈로그{#material-catalogs}

재질 카탈로그는 많은 이미지 렌더링 구성 설정을 제공합니다.

재질 카탈로그는 요청에 사용된 비네팅 및 재질 ID를 실제 파일 경로에 매핑하고, 자료와 관련된 모든 메타데이터를 저장하고, 템플릿에 대한 컨테이너를 제공할 수 있습니다. ICC 프로파일 및 명령 매크로를 추적합니다.

재질 카탈로그는 이미지 렌더링의 Java 구성 요소(와 함께 위치)에서만 액세스됩니다. [!DNL Platform Server]). 카탈로그 속성 파일에 [!DNL .ini] 접미사 및 등록된 카탈로그 폴더에 배치할 수 있습니다([ir.catalogRootPath](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-catalog-folder.md#concept-1c1d308112054bb99e3895c3fb8ca5f7)). 기본 재질 카탈로그( [!DNL default.ini])는 항상 존재해야 하며 이미지 제공의 올바른 작동을 위해 모든 속성으로 채워야 합니다.
