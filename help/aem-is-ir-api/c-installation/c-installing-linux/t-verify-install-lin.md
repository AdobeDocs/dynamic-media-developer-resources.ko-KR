---
title: 설치 확인
description: Linux®에 이미지 서비스를 설치한 후 설치를 확인합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 273478ab-f245-48ef-a125-fb738054484e
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---

# 설치 확인{#verifying-the-installation}

Linux®에 이미지 서비스를 설치한 후 설치를 확인합니다.

이미지 서버가 Linux® 데몬으로 설치됩니다.

**설치를 확인하려면**

1. 이미지 제공 서비스가 자동으로 시작되도록 구성되어 있고 실행 중인지 확인합니다.

   `> /sbin/service ImageServing status`

   >[!NOTE]
   >
   >이러한 스크립트를 실행하려면 루트 권한이 있어야 합니다.

1. 동일하거나 다른 호스트에서 인터넷 브라우저를 열고 기본 서버 응답을 확인합니다.

[!DNL http:// *[!DNL server:port]*/is/image]

[!DNL  http:// *[!DNL server:port]*/ir/render]

응답에서 `imageServer`: [!DNL Platform Server] 이미지 서버와 통신할 수 없습니다.

>설치된 경우 설명서 및 데모 패키지의 샘플 페이지를 사용하여 추가 확인을 수행할 수 있습니다.
