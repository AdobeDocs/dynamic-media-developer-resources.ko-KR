---
description: SSL에 대해 이러한 서버 설정을 사용합니다.
seo-description: SSL에 대해 이러한 서버 설정을 사용합니다.
seo-title: SSL
solution: Experience Manager
title: SSL
topic: Scene7 Image Serving - Image Rendering API
uuid: dec9bd09-8191-4010-8898-2890ffbe9ca7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SSL{#ssl}

SSL에 대해 이러한 서버 설정을 사용합니다.

## TC::SslPort - 수신 포트 {#section-c80eb582bf684b3fa7313a77cc606769}

SSL 연결에 대한 플랫폼 서버의 수신 포트를 지정합니다. 기본값은 8443입니다.

## TC::keystoreFile - Keystore 파일 경로 {#section-0cdf9b3cfcf249818b22221d01bafebe}

SSL 키 저장소 파일의 경로/이름을 지정합니다. 절대 경로이거나 [!DNL/conf]에 상대적인 경로일 *[!DNL install_folder]*&#x200B;수 있습니다. 기본값은 *install_folder*/conf/scene7keystore입니다.

## TC::keystorePass - Keystore 암호 {#section-e7e9bfb7df584a248c0e3ee46803c3b1}

키 저장소 파일의 암호입니다. Default is `scene7`.

## TC::keystoreType - Keystore Type {#section-8f263e1ba67740728cd39181960d7c7d}

키 저장소 유형을 선택합니다. &#39; `Java'` (기본값) 및 &#39; `PKCS12`&#39;가 지원됩니다.
