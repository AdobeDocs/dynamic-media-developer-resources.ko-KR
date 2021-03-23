---
description: Dynamic Media Image Serving을 설치한 후 설치를 확인해야 합니다.
seo-description: Dynamic Media Image Serving을 설치한 후 설치를 확인해야 합니다.
seo-title: 설치 확인
solution: Experience Manager
title: 설치 확인
uuid: ccc7688d-3d7f-4066-a19e-8a36ca56d711
feature: Dynamic Media Classic,SDK/API
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 0%

---


# 설치 확인 중{#verifying-the-installation}

Dynamic Media Image Serving을 설치한 후 설치를 확인해야 합니다.

이미지 서버가 Windows 서비스로 설치됩니다.

1. 서비스 Campaign 컨트롤 패널을 열고 &quot;Dynamic Media Image Serving&quot;이 &quot;Started&quot; 상태로 있는지 확인합니다.
1. 동일한 호스트 또는 다른 호스트에서 인터넷 브라우저를 열고 기본 서버 응답을 확인합니다.

   `http:// server:port /is/image`

[!DNL http:// *[!DNL server:port]*/ir/render]

응답에 &quot; `imageServer.`&quot; 항목이 있는지 확인합니다. 이 항목은 이미지 서버가 수신 대기 중임을 나타냅니다.
>설명서 및 데모 패키지의 샘플 페이지를 설치한 경우 추가 확인을 수행할 수 있습니다.

