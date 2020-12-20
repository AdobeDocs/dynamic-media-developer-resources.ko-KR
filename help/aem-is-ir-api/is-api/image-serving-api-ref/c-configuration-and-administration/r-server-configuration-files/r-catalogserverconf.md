---
description: 이미지 카탈로그 관리와 관련된 설정을 포함합니다.
seo-description: 이미지 카탈로그 관리와 관련된 설정을 포함합니다.
seo-title: catalog-server.conf
solution: Experience Manager
title: catalog-server.conf
topic: Scene7 Image Serving - Image Rendering API
uuid: 797a43d2-18f5-4735-8b19-da231952b1a2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 0%

---


# catalog-server.conf{#catalog-server-conf}

이미지 카탈로그 관리와 관련된 설정을 포함합니다.

이 파일은 JAVA 속성 파일입니다. 적절한 규약을 준수하기 위해서는 세심한 주의를 기울여야 한다.그렇지 않으면 플랫폼 서버를 시작하지 못할 수 있습니다. Windows 파일 경로에서 백슬래시 &#39;\&#39; 대신 이중 백슬래시 &#39;\\&#39; 또는 단일 슬래시 &#39;/&#39;를 사용하십시오. 백슬래시는 이 유형의 파일에서 이스케이프 문자로 사용됩니다.

이 파일에 대한 변경 사항은 파일을 저장한 후 바로 적용됩니다.

아래 나열된 설정만 [!DNL catalog-service.conf]에서 변경할 수 있습니다. 특정 설정이 없으면 파일의 아무 곳에나 추가할 수 있습니다. 각 설정의 인스턴스는 하나만 있을 수 있습니다.

`catalog.rootPath=./catalog`

`catalog.cacheRoot=./cache`

`catalog.modificationWaitTime=5000`

`catalog.refreshInterval=10000`
