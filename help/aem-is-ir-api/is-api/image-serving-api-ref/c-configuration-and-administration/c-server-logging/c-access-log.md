---
description: 에 대한 모든 HTTP 요청을 추적하는 기본 로그입니다. [!DNL Platform Server]. 이미지 렌더링이 활성화되면 해당 액세스 로그 데이터가 동일한 파일에 기록됩니다.
solution: Experience Manager
title: 액세스 로그
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e7f9d935-cb98-404c-8922-6420a4217733
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---

# 액세스 로그{#access-log}

에 대한 모든 HTTP 요청을 추적하는 기본 로그입니다. [!DNL Platform Server]. 이미지 렌더링이 활성화되면 해당 액세스 로그 데이터가 동일한 파일에 기록됩니다.

server.xml에 액세스 로그가 구성되어 있습니다.

>[!NOTE]
>
>이미지 제공용 클라이언트 트래픽( [!DNL /is/image/*]) 및 이미지 렌더링( [!DNL /ir/render/*]), 액세스 로그는 특정 내부 트래픽: 다음에 대한 액세스를 포함할 수 있습니다. [!DNL Platform Server] 카탈로그 시스템( [!DNL /is-catalog/*]), 캐시 공유 및 오류 리디렉션 요청( [!DNL /is/cache/*])에 배포된 다른 패키지에 액세스 [!DNL Platform Server]: Dynamic Media 뷰어( [!DNL /is-viewers/*])에서 제공하는 정적 트래픽 및 정적 콘텐츠 요청 [!DNL Platform Server] (예: [!DNL /is-docs/*]).

다음을 포함한 요청 [!DNL /is-catalog] 및 [!DNL /is/cache] 루트 경로는 항상 클라이언트 트래픽 분석에서 제외해야 합니다.
