---
description: 이미지 카탈로그는 글꼴, ICC 프로파일, 명령 매크로 등 다양한 서버 구성 설정을 제공합니다.
seo-description: 이미지 카탈로그는 글꼴, ICC 프로파일, 명령 매크로 등 다양한 서버 구성 설정을 제공합니다.
seo-title: 이미지 카탈로그
solution: Experience Manager
title: 이미지 카탈로그
topic: Scene7 Image Serving - Image Rendering API
uuid: 7d7285e2-ee9c-4e88-b270-b686d1984d82
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 이미지 카탈로그{#image-catalogs}

이미지 카탈로그는 글꼴, ICC 프로파일, 명령 매크로 등 다양한 서버 구성 설정을 제공합니다.

요청에 사용된 이미지 및 정적 컨텐츠 ID를 실제 파일 경로에 매핑하고, 이미지 맵과 같은 다양한 이미지 메타데이터를 저장하고, 템플릿 및 이미지 세트에 대한 컨테이너를 제공합니다.

이미지 카탈로그는 이미지 서버가 아닌 플랫폼 서버에서만 액세스합니다. 카탈로그 특성 파일은 .ini 접미사를 가져야 하며 플랫폼 서버의 카탈로그 폴더( `PS::CatalogFolder`)에 배치됩니다. 적어도 기본 이미지 카탈로그는 필수이며 플랫폼 서버의 올바른 기능을 위해 모든 속성으로 채워야 합니다.
