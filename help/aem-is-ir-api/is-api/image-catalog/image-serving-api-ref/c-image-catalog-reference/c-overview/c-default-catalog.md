---
description: 기본 카탈로그는 모든 이미지 카탈로그의 모든 카탈로그 속성에 대한 기본값을 제공합니다.
solution: Experience Manager
title: 기본 카탈로그
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: db42fb67-aa6f-4217-bc69-45b01bbd0b10
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---

# 기본 카탈로그{#default-catalog}

기본 카탈로그는 모든 이미지 카탈로그의 모든 카탈로그 속성에 대한 기본값을 제공합니다.

특정 이미지 카탈로그에서 특정 속성을 찾을 수 없는 경우 서버는 기본 카탈로그의 해당 값을 대신 사용합니다. 마찬가지로 기본 카탈로그를 사용하여 특정 카탈로그 데이터 레코드(이미지, 매크로 정의, 글꼴 및 ICC 프로파일)에 대한 기본값을 제공할 수 있습니다. 특정 이미지 카탈로그에서 특정 데이터 레코드를 찾을 수 없는 경우, 서버는 대신 기본 카탈로그에서 해당 데이터 레코드를 찾으려고 시도합니다. 따라서 이미지 카탈로그를 간단히 작성하고 공유 템플릿, 매크로, 글꼴 등과 같은 글로벌 속성 및 데이터를 간편하게 관리할 수 있습니다.

또한 특정 이미지 카탈로그가 작업에 포함되지 않은 경우 기본 카탈로그는 모든 속성 및 데이터 레코드(매크로, 글꼴, ICC 프로파일, 요청 전처리 규칙)를 제공합니다.

[!DNL Platform Server]이(가) 올바르게 작동하려면 기본 카탈로그의 카탈로그 특성 파일 이름이 [!DNL default.ini]이고, 카탈로그 폴더에 항상 있어야 하며, `attribute::RootId`과(와) 다양한 카탈로그 데이터 파일에 대한 참조(모두 선택 사항)를 제외한 모든 필수 특성으로 완전히 채워야 합니다.

>[!NOTE]
>
>[!DNL default.ini]을(를) 제외한 모든 카탈로그 특성 파일에는 고유한 `attribute::RootId` 값이 있어야 합니다. [!DNL default.ini]의 `attribute::RootId`은(는) 비어 있어야 합니다.
