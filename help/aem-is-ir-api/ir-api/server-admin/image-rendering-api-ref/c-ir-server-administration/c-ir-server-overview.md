---
description: 이 설명서에서는 Dynamic Media 이미지 렌더링 서버를 관리하는 방법을 설명합니다.
solution: Experience Manager
title: 서버 관리 개요
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 294cd068-8676-4932-a3ad-1a3c5bfa691e
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---

# 서버 관리 개요{#server-administration-overview}

이 설명서에서는 Dynamic Media 이미지 렌더링 서버를 관리하는 방법을 설명합니다.

이미지 렌더링은 다음 두 가지 주요 구성 요소로 구성됩니다.

* 이미지 제공과 함께 Java 패키지가 배포됩니다 [!DNL Platform Server] 클라이언트 연결, 캐싱, 자료 카탈로그를 관리합니다.
* 기본 코드 모듈은 이미지 서버용 확장 라이브러리로 배포되고 핵심 이미지 렌더링 기능을 구현합니다.

두 구성 요소를 통칭하여 라고 합니다. *렌더링 서버*.

이미지 렌더링은 이미지 제공과 많은 서버 기능을 공유하며, 모든 옵션은 구성 파일을 편집하여 구성됩니다. 추가 구성 속성은 기본 카탈로그에서 제공됩니다( [!DNL default.ini]) 또는 특정 재질 카탈로그. 자세한 내용은 자재 카탈로그 를 참조하십시오.

이미지 렌더링 설치 폴더( *[!DNL install_folder]*) [!DNL *[!DNL install_root]*/ImageRendering] Windows의 경우 기본값 *[!DNL install_root]* 은(는) `C:\Program Files\Scene7`. 설치하는 동안 다른 폴더를 지정할 수 있습니다. Linux에서 *[!DNL install_root]* 은(는) 항상 [!DNL /usr/local/scene7]. 심볼 링크를 사용할 수 있습니다.

모든 파일 경로는 UNIX에서는 대/소문자를 구분하고 Windows에서는 대/소문자를 구분하지 않습니다.
