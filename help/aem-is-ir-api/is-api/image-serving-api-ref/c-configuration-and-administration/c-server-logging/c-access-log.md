---
description: ' [!DNL Platform Server]에 대한 모든 HTTP 요청을 추적하는 기본 로그입니다. 이미지 렌더링이 활성화되면 해당 액세스 로그 데이터가 동일한 파일에 기록됩니다.'
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

[!DNL Platform Server]에 대한 모든 HTTP 요청을 추적하는 기본 로그입니다. 이미지 렌더링이 활성화되면 해당 액세스 로그 데이터가 동일한 파일에 기록됩니다.

server.xml에 액세스 로그가 구성되어 있습니다.

>[!NOTE]
>
>이미지 제공([!DNL /is/image/*]) 및 이미지 렌더링([!DNL /ir/render/*])에 대한 클라이언트 트래픽 외에도, 액세스 로그에는 특정 내부 트래픽, 즉 [!DNL Platform Server] 카탈로그 시스템에 대한 액세스([!DNL /is-catalog/*]), 캐시 공유 및 오류 리디렉션 요청([!DNL /is/cache/*]), Dynamic Media 뷰어([!DNL Platform Server])와 같은 [!DNL /is-viewers/*]에 배포된 다른 패키지에 대한 액세스, [!DNL Platform Server]에서 서비스하는 정적 트래픽 및 정적 콘텐츠 요청(예: [!DNL /is-docs/*])이 포함될 수 있습니다.

[!DNL /is-catalog] 및 [!DNL /is/cache] 루트 경로가 있는 요청은 항상 클라이언트 트래픽 분석에서 제외해야 합니다.
