---
title: 설치 확인
description: Dynamic Media 이미지 서비스를 설치한 후 설치를 확인해야 합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3fcb1f20-8334-497e-8b3e-9097751ca5c1
TQID: 'https://experienceleague.adobe.com/2i1-Ncy7lyIbm8BHFZGVLNIDnZUOA9sr3tZ970WswL4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 104
ht-degree: 0%

---

# 설치 확인 {#verifying-the-installation}

Dynamic Media 이미지 서비스를 설치한 후 설치를 확인해야 합니다.

이미지 서버는 Windows 서비스로 설치됩니다.

1. 서비스 Campaign 컨트롤 패널을 열고 `Dynamic Media Image Serving`이(가) `Started` 상태로 있는지 확인하십시오.
1. 동일한 호스트 또는 다른 호스트에서 인터넷 브라우저를 열고 기본 서버 응답을 확인합니다.

   `http:// server:port /is/image`

[!DNL  http:// *[!DNL server:port]*/ir/render]

응답에 이미지 서버가 수신 중임을 나타내는 &quot; `imageServer.`&quot; 항목이 있는지 확인합니다.

>설명서 및 데모 패키지(설치된 경우)의 샘플 페이지를 사용하여 추가 확인을 수행할 수 있습니다.

