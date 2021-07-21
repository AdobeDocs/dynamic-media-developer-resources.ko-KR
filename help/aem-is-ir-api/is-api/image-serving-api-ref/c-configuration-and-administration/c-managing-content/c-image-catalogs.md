---
description: 이미지 카탈로그는 글꼴, ICC 프로필, 명령 매크로와 함께 많은 서버 구성 설정을 제공합니다.
solution: Experience Manager
title: 이미지 카탈로그
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 70ec4566-a937-464e-8219-b7eda3ab66c1
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---

# 이미지 카탈로그{#image-catalogs}

이미지 카탈로그는 글꼴, ICC 프로필, 명령 매크로와 함께 많은 서버 구성 설정을 제공합니다.

요청에 사용된 이미지 및 정적 콘텐츠 ID를 실제 파일 경로에 매핑하고, 이미지 맵과 같은 다양한 이미지 메타데이터를 저장하고, 템플릿 및 이미지 세트에 대한 컨테이너를 제공합니다.

이미지 카탈로그는 이미지 서버가 아닌 Platform Server에서만 액세스할 수 있습니다. 카탈로그 특성 파일에는 .ini 접미사가 있어야 하며 Platform Server의 카탈로그 폴더( `PS::CatalogFolder`)에 배치되어야 합니다. 최소한 기본 이미지 카탈로그가 필요하며 Platform Server의 올바른 기능을 위해서는 모든 특성을 채워야 합니다.
