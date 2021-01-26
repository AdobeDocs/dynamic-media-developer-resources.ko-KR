---
description: 이 문서에서는 Dynamic Media 이미지 렌더링 서버를 관리하는 방법에 대해 설명합니다.
seo-description: 이 문서에서는 Dynamic Media 이미지 렌더링 서버를 관리하는 방법에 대해 설명합니다.
seo-title: 서버 관리 개요
solution: Experience Manager
title: 서버 관리 개요
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 83aa83b7-bb7a-4bbd-923c-dd69763fe9c9
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 0%

---


# 서버 관리 개요{#server-administration-overview}

이 문서에서는 Dynamic Media 이미지 렌더링 서버를 관리하는 방법에 대해 설명합니다.

이미지 렌더링은 두 가지 주요 구성 요소로 이루어집니다.

* Java 패키지는 Image Serving Platform Server와 함께 배포되고 클라이언트 연결, 캐싱, 재질 카탈로그를 관리합니다.
* 기본 코드 모듈은 이미지 서버용 확장 라이브러리로 배포되고 핵심 이미지 렌더링 기능을 구현합니다.

두 구성 요소를 모두 *Render Server*&#x200B;라고 통칭합니다.

이미지 렌더링은 많은 서버 시설과 이미지 제공 기능을 공유하고 구성 파일을 편집하여 모든 옵션을 구성합니다. 추가 구성 속성은 기본 카탈로그( [!DNL default.ini]) 또는 특정 자료 카탈로그에 의해 제공됩니다. 자세한 내용은 자료 카탈로그를 참조하십시오.

이미지 렌더링 설치 폴더( *[!DNL install_folder]*)는 [!DNL *[!DNL install_root]*/ImageRendering]입니다. Windows의 경우 기본 *[!DNL install_root]*&#x200B;은 `C:\Program Files\Scene7`입니다. 설치하는 동안 다른 폴더를 지정할 수 있습니다. Linux에서 *[!DNL install_root]*&#x200B;은(는) 항상 [!DNL /usr/local/scene7]이어야 합니다. 상징적 링크를 사용할 수 있습니다.

모든 파일 경로는 UNIX에서는 대/소문자를 구분하며 Windows에서는 대/소문자를 구분하지 않습니다.
