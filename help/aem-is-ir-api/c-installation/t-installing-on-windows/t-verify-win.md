---
description: Dynamic Media 이미지 제공 서비스를 설치한 후 설치를 확인해야 합니다.
solution: Experience Manager
title: 설치 확인
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 3fcb1f20-8334-497e-8b3e-9097751ca5c1
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---

# 설치 확인{#verifying-the-installation}

Dynamic Media 이미지 제공 서비스를 설치한 후 설치를 확인해야 합니다.

이미지 서버가 Windows 서비스로 설치됩니다.

1. 서비스 Campaign 컨트롤 패널을 열고 &quot;Dynamic Media 이미지 제공&quot;이 &quot;시작됨&quot; 상태로 있는지 확인합니다.
1. 동일하거나 다른 호스트에서 인터넷 브라우저를 열고 기본 서버 응답을 확인합니다.

   `http:// server:port /is/image`

[!DNL http:// *[!DNL server:port]*/ir/render]

응답에 이미지 서버가 수신 중임을 나타내는 &quot; `imageServer.`&quot; 항목이 있는지 확인합니다.
>설치된 경우 설명서 및 데모 패키지의 샘플 페이지를 사용하여 추가 확인을 수행할 수 있습니다.
