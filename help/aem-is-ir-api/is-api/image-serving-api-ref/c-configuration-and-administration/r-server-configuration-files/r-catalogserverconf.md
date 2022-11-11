---
description: 이미지 카탈로그 관리와 관련된 설정을 포함합니다.
solution: Experience Manager
title: catalog-server.conf
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 55e55381-3828-4937-8746-a74e82d6ca38
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 0%

---

# catalog-server.conf{#catalog-server-conf}

이미지 카탈로그 관리와 관련된 설정을 포함합니다.

이 파일은 JAVA 속성 파일입니다. 적절한 규약을 준수하기 위해서는 주의해야 합니다. 그렇지 않으면 [!DNL Platform Server] 시작되지 않을 수 있습니다. Windows 파일 경로에 백슬래시 &#39;\&#39; 대신 이중 백슬래시 &#39;\\&#39; 또는 단일 슬래시 &#39;/&#39;를 사용하십시오. 백슬래시는 이 유형의 파일에서 이스케이프 문자로 사용됩니다.

이 파일의 변경 사항은 파일을 저장한 직후에 적용됩니다.

아래에 나열된 설정만 [!DNL catalog-service.conf]. 특정 설정이 없으면 파일의 아무 곳에나 추가할 수 있습니다. 각 설정의 인스턴스는 하나만 있을 수 있습니다.

`catalog.rootPath=./catalog`

`catalog.cacheRoot=./cache`

`catalog.modificationWaitTime=5000`

`catalog.refreshInterval=10000`
