---
description: 재료 카탈로그는 많은 이미지 렌더링 구성 설정을 제공합니다.
seo-description: 재료 카탈로그는 많은 이미지 렌더링 구성 설정을 제공합니다.
seo-title: 재료 카탈로그
solution: Experience Manager
title: 재료 카탈로그
topic: Scene7 Image Serving - Image Rendering API
uuid: 6d209019-f9ca-43e4-900b-3597c7044a79
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 재료 카탈로그{#material-catalogs}

재료 카탈로그는 많은 이미지 렌더링 구성 설정을 제공합니다.

재료 카탈로그는 비네팅 및 요청에 사용된 자재 ID를 실제 파일 경로에 매핑하고, 자료와 관련된 모든 메타데이터를 저장하고, 템플릿에 대한 컨테이너를 제공할 수 있습니다. ICC 프로파일과 명령 매크로를 추적할 수 있습니다.

자료 카탈로그는 이미지 렌더링의 Java 구성 요소(플랫폼 서버와 함께 위치)만 액세스합니다. 카탈로그 속성 파일은 [!DNL .ini] 접미사를 가져야 하며 등록된 카탈로그 폴더([ir.catalogRootPath)에 삽입해야 합니다](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-catalog-folder.md#concept-1c1d308112054bb99e3895c3fb8ca5f7). 기본 재료 카탈로그( [!DNL default.ini])는 항상 존재해야 하며 이미지 제공의 올바른 기능을 위해 모든 속성으로 채워야 합니다.
