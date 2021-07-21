---
description: Platform Server에 대한 모든 HTTP 요청을 추적하는 기본 로그입니다. 이미지 렌더링이 활성화되어 있으면 해당 액세스 로그 데이터를 동일한 파일에 씁니다.
solution: Experience Manager
title: 액세스 로그
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e7f9d935-cb98-404c-8922-6420a4217733
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---

# 액세스 로그{#access-log}

Platform Server에 대한 모든 HTTP 요청을 추적하는 기본 로그입니다. 이미지 렌더링이 활성화되어 있으면 해당 액세스 로그 데이터를 동일한 파일에 씁니다.

액세스 로그는 server.xml에 구성되어 있습니다.

>[!NOTE]
>
>액세스 로그에는 이미지 제공( [!DNL /is/image/*]) 및 이미지 렌더링( [!DNL /ir/render/*])에 대한 클라이언트 트래픽 외에도 특정 내부 트래픽이 포함될 수 있습니다. Platform Server 카탈로그 시스템( [!DNL /is-catalog/*])에 대한 액세스, 캐시 공유 및 오류 리디렉션 요청( [!DNL /is/cache/*]), Dynamic Media 뷰어( [!DNL /is-viewers/*])와 같이 Platform Server에 배포된 다른 패키지에 대한 액세스, Platform Server에서 제공하는 정적 트래픽 및 정적 컨텐츠 요청(예: [!DNL /is-docs/*]).

[!DNL /is-catalog] 및 [!DNL /is/cache] 루트 경로를 사용하는 요청은 항상 클라이언트 트래픽 분석에서 제외되어야 합니다.
