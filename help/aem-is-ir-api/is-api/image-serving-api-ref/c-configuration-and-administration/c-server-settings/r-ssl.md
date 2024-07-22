---
description: SSL에 대해 이러한 서버 설정을 사용합니다.
solution: Experience Manager
title: SSL
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 4a5c52cc-de47-48e0-ac92-6ee66a58a7ea
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 2%

---

# SSL{#ssl}

SSL에 대해 이러한 서버 설정을 사용합니다.

## TC::SslPort - 수신 포트 {#section-c80eb582bf684b3fa7313a77cc606769}

SSL 연결을 위한 [!DNL Platform Server]의 수신 대기 포트를 지정합니다. 기본값은 8443입니다.

## TC::keystoreFile - Keystore 파일 경로 {#section-0cdf9b3cfcf249818b22221d01bafebe}

SSL 키 저장소 파일의 경로/이름을 지정합니다. 절대 경로이거나 [!DNL *[!DNL install_folder]*/conf]에 상대적인 경로일 수 있습니다. 기본값은 *install_folder*/conf/scene7keystore입니다.

## TC::keystorePass - 키 저장소 암호 {#section-e7e9bfb7df584a248c0e3ee46803c3b1}

키 저장소 파일의 암호입니다. 기본값은 `scene7`입니다.

## TC::keystoreType - Keystore 유형 {#section-8f263e1ba67740728cd39181960d7c7d}

키 저장소 유형을 선택합니다. &#39; `Java'`(기본값) 및 &#39; `PKCS12`&#39;이(가) 지원됩니다.
