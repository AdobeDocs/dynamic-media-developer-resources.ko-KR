---
description: 기본 카탈로그는 모든 이미지 카탈로그에 대한 모든 카탈로그 속성의 기본값을 제공합니다.
solution: Experience Manager
title: 기본 카탈로그
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: db42fb67-aa6f-4217-bc69-45b01bbd0b10
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---

# 기본 카탈로그{#default-catalog}

기본 카탈로그는 모든 이미지 카탈로그에 대한 모든 카탈로그 속성의 기본값을 제공합니다.

특정 이미지 카탈로그에서 특정 속성을 찾을 수 없는 경우 서버는 대신 기본 카탈로그의 해당 값을 사용합니다. 마찬가지로 기본 카탈로그를 사용하여 특정 카탈로그 데이터 레코드(이미지, 매크로 정의, 글꼴 및 ICC 프로필)의 기본값을 제공할 수 있습니다. 특정 이미지 카탈로그에서 특정 데이터 레코드를 찾을 수 없는 경우, 서버가 대신 기본 카탈로그에서 해당 레코드를 찾습니다. 이렇게 하면 공유 템플릿, 매크로, 글꼴 등과 같은 글로벌 속성과 데이터를 쉽게 관리하고 이미지 카탈로그를 제한적으로 채울 수 있습니다.

또한 특정 이미지 카탈로그가 작업에 포함되어 있지 않을 경우 기본 카탈로그는 모든 속성 및 데이터 레코드(매크로, 글꼴, ICC 프로필, 사전 처리 규칙 요청)를 제공합니다.

Platform Server가 올바르게 작동하려면 기본 카탈로그의 카탈로그 특성 파일의 이름을 [!DNL default.ini]으로 지정해야 하며, 항상 카탈로그 폴더에 있어야 하며, 모든 필수 속성(모두 선택 사항인 `attribute::RootId` 및 다양한 카탈로그 데이터 파일에 대한 참조를 제외)으로 채워야 합니다.

>[!NOTE]
>
>[!DNL default.ini]을 제외한 모든 카탈로그 특성 파일에는 고유한 `attribute::RootId` 값이 있어야 합니다. `attribute::RootId` 에서 [!DNL default.ini] 는 비어 있어야 합니다.
