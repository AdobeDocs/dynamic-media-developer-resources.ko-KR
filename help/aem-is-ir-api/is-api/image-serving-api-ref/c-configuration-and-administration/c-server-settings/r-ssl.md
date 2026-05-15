---
description: SSL에 대해 이러한 서버 설정을 사용합니다.
solution: Experience Manager
title: SSL
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 4a5c52cc-de47-48e0-ac92-6ee66a58a7ea
TQID: 'https://experienceleague.adobe.com/VOdDIzV6b9J9AZ-qZyAj3AI77MukT1BbSzM-UM-B5N4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 86
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
