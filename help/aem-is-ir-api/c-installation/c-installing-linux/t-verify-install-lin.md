---
description: Linux에서 이미지 제공을 설치한 후 설치를 확인합니다.
seo-description: Linux에서 이미지 제공을 설치한 후 설치를 확인합니다.
seo-title: 설치 확인
solution: Experience Manager
title: 설치 확인
topic: Scene7 Image Serving - Image Rendering API
uuid: 4fdf61c7-3c9f-4f3e-9696-60eb7e3f2209
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 설치 확인{#verifying-the-installation}

Linux에서 이미지 제공을 설치한 후 설치를 확인합니다.

이미지 서버는 Linux 데몬으로 설치됩니다.

**설치를 확인하려면**

1. Image Serving이 자동으로 시작되도록 구성되었고 실행 중인지 확인합니다.

   `> /sbin/service ImageServing status`

   >[!NOTE] {class=&quot;- topic/note &quot;}
   >
   >이러한 스크립트를 실행하려면 루트 권한이 있어야 합니다.

1. 동일한 호스트 또는 다른 호스트에서 인터넷 브라우저를 열고 기본 서버 응답을 확인합니다.

[!DNL http:// *[!DNL server:port]*/is/image]

[!DNL http:// *[!DNL server:port]*/ir/render]

응답에서 플랫폼 서버가 이미지 서버와 성공적으로 통신할 수 있음을 나타내는 &quot; `imageServer.`&quot;로 시작하는 항목이 있는지 확인합니다.
>설치 시 설명서 및 데모 패키지의 샘플 페이지를 사용하여 추가 확인을 수행할 수 있습니다.

