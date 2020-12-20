---
description: 플랫폼 서버에 대한 모든 HTTP 요청을 추적하는 기본 로그입니다. 이미지 렌더링이 활성화되면 해당 액세스 로그 데이터를 동일한 파일에 씁니다.
seo-description: 플랫폼 서버에 대한 모든 HTTP 요청을 추적하는 기본 로그입니다. 이미지 렌더링이 활성화되면 해당 액세스 로그 데이터를 동일한 파일에 씁니다.
seo-title: 액세스 로그
solution: Experience Manager
title: 액세스 로그
topic: Scene7 Image Serving - Image Rendering API
uuid: 33cd4338-1fe7-46ac-83f5-200ea26f1e22
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 0%

---


# 액세스 로그{#access-log}

플랫폼 서버에 대한 모든 HTTP 요청을 추적하는 기본 로그입니다. 이미지 렌더링이 활성화되면 해당 액세스 로그 데이터를 동일한 파일에 씁니다.

액세스 로그는 server.xml에서 구성됩니다.

>[!NOTE]
>
>이미지 제공( [!DNL /is/image/*]) 및 이미지 렌더링( [!DNL /ir/render/*])에 대한 클라이언트 트래픽 외에도 액세스 로그에 특정 내부 트래픽이 포함될 수 있습니다.플랫폼 서버 카탈로그 시스템( [!DNL /is-catalog/*]) 액세스, 캐시 공유 및 오류 리디렉션 요청( [!DNL /is/cache/*]), Scene7 뷰어( [!DNL /is-viewers/*]) 등 플랫폼 서버에 배포된 다른 패키지에 대한 액세스, 플랫폼 서버에서 제공하는 정적 트래픽 및 정적 컨텐츠 요청(예:[!DNL /is-docs/*]).

[!DNL /is-catalog] 및 [!DNL /is/cache] 루트 경로가 있는 요청은 항상 클라이언트 트래픽 분석에서 제외되어야 합니다.
