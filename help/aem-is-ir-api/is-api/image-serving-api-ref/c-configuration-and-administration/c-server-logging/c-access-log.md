---
description: 플랫폼 서버에 대한 모든 HTTP 요청을 추적하는 기본 로그입니다. 이미지 렌더링이 활성화되면 해당 액세스 로그 데이터를 동일한 파일에 씁니다.
solution: Experience Manager
title: 액세스 로그
feature: Dynamic Media Classic,SDK/API
role: 개발자,관리자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 0%

---


# 액세스 로그{#access-log}

플랫폼 서버에 대한 모든 HTTP 요청을 추적하는 기본 로그입니다. 이미지 렌더링이 활성화되면 해당 액세스 로그 데이터를 동일한 파일에 씁니다.

액세스 로그는 server.xml에서 구성됩니다.

>[!NOTE]
>
>이미지 제공( [!DNL /is/image/*]) 및 이미지 렌더링( [!DNL /ir/render/*])에 대한 클라이언트 트래픽 외에도 액세스 로그에 특정 내부 트래픽이 포함될 수 있습니다.플랫폼 서버 카탈로그 시스템( [!DNL /is-catalog/*]) 액세스, 캐시 공유 및 오류 리디렉션 요청( [!DNL /is/cache/*]), Dynamic Media 뷰어( [!DNL /is-viewers/*]) 등 플랫폼 서버에 배포된 다른 패키지에 대한 액세스, 플랫폼 서버에서 제공하는 정적 트래픽 및 정적 컨텐츠 요청(예:[!DNL /is-docs/*]).

[!DNL /is-catalog] 및 [!DNL /is/cache] 루트 경로가 있는 요청은 항상 클라이언트 트래픽 분석에서 제외되어야 합니다.
