---
description: 기본 카탈로그는 모든 이미지 카탈로그에 대한 모든 카탈로그 속성의 기본값을 제공합니다.
seo-description: 기본 카탈로그는 모든 이미지 카탈로그에 대한 모든 카탈로그 속성의 기본값을 제공합니다.
seo-title: 기본 카탈로그
solution: Experience Manager
title: 기본 카탈로그
topic: Scene7 Image Serving - Image Rendering API
uuid: 9f0c967e-a2fa-4ef0-bacb-3dcfb06a8027
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 기본 카탈로그{#default-catalog}

기본 카탈로그는 모든 이미지 카탈로그에 대한 모든 카탈로그 속성의 기본값을 제공합니다.

특정 이미지 카탈로그에서 특정 속성을 찾을 수 없는 경우 서버는 대신 기본 카탈로그의 해당 값을 사용합니다. 마찬가지로 기본 카탈로그를 사용하여 특정 카탈로그 데이터 레코드(이미지, 매크로 정의, 글꼴 및 ICC 프로파일)에 대한 기본값을 제공할 수 있습니다. 특정 데이터 레코드를 특정 이미지 카탈로그에서 찾을 수 없는 경우 서버가 대신 기본 카탈로그에서 해당 레코드를 찾으려고 시도합니다. 이렇게 하면 이미지 카탈로그가 드물게 채워지고 공유 템플릿, 매크로, 글꼴 등과 같은 전역 특성 및 데이터 관리를 간소화할 수 있습니다.

또한 기본 카탈로그는 특정 이미지 카탈로그가 작업에 관련되지 않은 경우 모든 특성 및 데이터 레코드(매크로, 글꼴, ICC 프로필, 사전 처리 규칙 요청)를 제공합니다.

Platform Server의 올바른 기능을 위해서는 기본 카탈로그에 대한 카탈로그 속성 파일의 이름이 [!DNL default.ini]지정되어야 하며, 항상 카탈로그 폴더에 있어야 하며, 모든 필수 속성(선택 사항) `attribute::RootId` 과 다양한 카탈로그 데이터 파일에 대한 참조를 제외한 모든 필수 속성으로 채워야 합니다.

>[!NOTE]
>
>을 제외한 모든 카탈로그 속성 파일에는 고유 [!DNL default.ini] 값이 `attribute::RootId` 포함되어야 합니다. `attribute::RootId` in [!DNL default.ini] 은 비어 있어야 합니다.

