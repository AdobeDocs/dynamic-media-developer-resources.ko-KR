---
description: 기본 로그로서, [!DNL Platform Server]. 이미지 렌더링이 활성화되어 있으면 해당 액세스 로그 데이터를 동일한 파일에 씁니다.
solution: Experience Manager
title: 액세스 로그
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e7f9d935-cb98-404c-8922-6420a4217733
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# 액세스 로그{#access-log}

기본 로그로서, [!DNL Platform Server]. 이미지 렌더링이 활성화되어 있으면 해당 액세스 로그 데이터를 동일한 파일에 씁니다.

액세스 로그는 server.xml에 구성되어 있습니다.

>[!NOTE]
>
>이미지 제공 ( [!DNL /is/image/*]) 및 이미지 렌더링( [!DNL /ir/render/*]), 액세스 로그에는 특정 내부 트래픽이 포함될 수 있습니다. 액세스 권한 [!DNL Platform Server] 카탈로그 시스템 ( [!DNL /is-catalog/*]), 캐시 공유 및 오류 리디렉션 요청( ) [!DNL /is/cache/*]), 에 배포된 다른 패키지에 대한 액세스 [!DNL Platform Server]( 예: Dynamic Media 뷰어 ( [!DNL /is-viewers/*]), 정적 트래픽 및 [!DNL Platform Server] (예: [!DNL /is-docs/*]).

요청이 있는 경우 [!DNL /is-catalog] 및 [!DNL /is/cache] 루트 경로는 항상 클라이언트 트래픽 분석에서 제외해야 합니다.
