---
title: 설치 확인
description: Linux®에 이미지 서비스를 설치한 후 설치를 확인합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 273478ab-f245-48ef-a125-fb738054484e
TQID: 'https://experienceleague.adobe.com/LyHlwiFL1b-iwo1kSnUeNfNo3fZY6FZetHgnNFoxGZo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 118
ht-degree: 0%

---

# 설치 확인{#verifying-the-installation}

Linux®에 이미지 서비스를 설치한 후 설치를 확인합니다.

이미지 서버는 Linux® 데몬으로 설치됩니다.

**설치를 확인하려면**

1. 이미지 제공이 자동으로 시작되도록 구성되어 있고 실행 중인지 확인합니다.

   `> /sbin/service ImageServing status`

   >[!NOTE]
   >
   >이러한 스크립트를 실행하려면 루트 권한이 있어야 합니다.

1. 동일한 호스트 또는 다른 호스트에서 인터넷 브라우저를 열고 기본 서버 응답을 확인합니다.

[!DNL http:// *[!DNL server:port]*/is/image]

[!DNL &#x200B; http:// *[!DNL server:port]*/ir/render]

응답에서 [!DNL Platform Server]이(가) 이미지 서버와 성공적으로 통신할 수 있음을 나타내는 `imageServer`(으)로 시작하는 항목이 있는지 확인합니다.

>설명서 및 데모 패키지(설치된 경우)의 샘플 페이지를 사용하여 추가 확인을 수행할 수 있습니다.
