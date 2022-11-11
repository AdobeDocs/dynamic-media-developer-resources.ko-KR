---
description: '이미지 카탈로그는 이미지 및 지원 데이터(예: 글꼴 및 ICC 프로필)에 대한 정보를 서버에 제공하는 데 사용됩니다.'
solution: Experience Manager
title: 개요
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 36cdd833-6fcb-4be6-a4f8-ba8d20580f29
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 0%

---

# 개요{#overview}

이미지 카탈로그는 이미지 및 지원 데이터(예: 글꼴 및 ICC 프로필)에 대한 정보를 서버에 제공하는 데 사용됩니다.

이미지 카탈로그는 이미지 및 지원 데이터(예: 글꼴 및 ICC 프로필)에 대한 정보를 서버에 제공하는 데 사용됩니다.

각 이미지 카탈로그는 필수 카탈로그 속성 파일과 선택적 카탈로그 데이터 파일 세트로 구성됩니다.

* 이미지 및 템플릿 및 관련 메타데이터를 항목별로 표시하는 이미지 데이터 파일입니다.
* SVG 파일 및 관련 메타데이터를 항목별로 표시하는 SVG 데이터 파일입니다.
* 요청 매크로에 대한 정의를 제공하는 매크로 정의 파일입니다.
* 텍스트 글꼴을 추적하는 글꼴 맵 파일입니다.
* ICC 색상 프로파일을 항목화하는 프로파일 맵 파일입니다.
* HTTP 요청 사전 처리 규칙을 정의하는 규칙 세트 파일입니다.

카탈로그 데이터 파일은 카탈로그 속성 파일의 파일 참조별로 이미지 카탈로그와 연결됩니다. 동일한 카탈로그 데이터 파일은 여러 이미지 카탈로그로 공유할 수 있습니다.

카탈로그 특성 파일에는 [!DNL .ini] 파일 접미사 및 [!DNL Platform Server]의 카탈로그 폴더( `PlatformServer::catalog.rootPath`). 카탈로그 데이터 파일은 동일한 폴더 또는 [!DNL Platform Server].

이 문서에서는 Dynamic Media 이미지 제공 시스템의 이미지 카탈로그 파일 형식에 대해 설명합니다. 의도한 대상은 웹 또는 사용자 지정 애플리케이션에서 Dynamic Media Image Serving을 활용하려는 숙련된 프로그래머 및 웹 사이트 개발자입니다.

일반적으로 리더는 Dynamic Media 이미지 제공 시스템, 일반 HTTP 프로토콜 표준 및 규칙, 기본 이미징 용어에 익숙하다고 가정합니다.
