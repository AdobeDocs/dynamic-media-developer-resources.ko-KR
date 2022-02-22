---
title: Linux®에서 시작 또는 중지
description: Linux®에서 이미지 서비스를 시작하거나 중지하기 위한 두 가지 옵션이 있습니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: eb4c60b2-5491-40e9-b105-d4b05006a9ca
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 0%

---

# Linux®에서 시작 또는 중지 {#starting-or-stopping-on-linux}

Linux®에서 이미지 서비스를 시작하거나 중지하기 위한 두 가지 옵션이 있습니다.

* 이미지 제공 상태를 확인하거나 이미지 제공 시작 및 중지 스크립트를 [!DNL ImageServing/bin] 폴더:

   `ImageServing.sh {start|stop|restart|status}`
* 시스템 관리자에게는 다음 대체 방법을 잘 알고 있어야 합니다.

   `/sbin/service ImageServing {start|stop|status}`
