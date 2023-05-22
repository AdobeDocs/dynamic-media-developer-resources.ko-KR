---
description: 이미지 카탈로그는 글꼴, ICC 프로파일, 명령 매크로뿐만 아니라 다양한 서버 구성 설정을 제공합니다.
solution: Experience Manager
title: 이미지 카탈로그
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 70ec4566-a937-464e-8219-b7eda3ab66c1
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---

# 이미지 카탈로그{#image-catalogs}

이미지 카탈로그는 글꼴, ICC 프로파일, 명령 매크로뿐만 아니라 다양한 서버 구성 설정을 제공합니다.

요청에 사용되는 이미지 및 정적 콘텐츠 ID를 실제 파일 경로에 매핑하고, 이미지 맵과 같은 다양한 이미지 메타데이터를 저장하고, 템플릿 및 이미지 세트에 대한 컨테이너를 제공합니다.

이미지 카탈로그는 [!DNL Platform Server]이미지 서버에서는 제공되지 않습니다. 카탈로그 속성 파일은 .ini 접미사를 사용하고 [!DNL Platform Server]의 카탈로그 폴더( `PS::CatalogFolder`). 최소한 기본 이미지 카탈로그가 필요하며 의 올바른 작동을 위해 모든 속성으로 채워야 합니다. [!DNL Platform Server].
