---
description: 정적 콘텐츠 소스 데이터 파일은 Platform Server에서만 액세스할 수 있습니다.
solution: Experience Manager
title: 정적 콘텐츠 소스 데이터
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 3cf01fc2-c925-4039-8e03-cb909cca6a51
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---

# 정적 콘텐츠 소스 데이터{#static-content-source-data}

정적 콘텐츠 소스 데이터 파일은 Platform Server에서만 액세스할 수 있습니다.

정적 콘텐츠 데이터 파일의 경로는 다음과 같이 해결됩니다.

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

서버는 절대 파일 경로가 설정될 때까지 경로 세그먼트를 오른쪽에서 왼쪽으로 결합합니다.

모든 ` *[!DNL rootPath]*` 세그먼트는 비어 있거나, 상대 또는 절대 경로 세그먼트일 수 있습니다.

` *[!DNL catalogPath]*` 는 절대 또는 상대 파일 경로/이름입니다. *[!DNL requestPath]* 상대 파일 경로/이름이어야 합니다.

[!DNL PlatformServer.conf]에서 여러 `PS::staticContent.rootPaths` 값을 정의할 수 있습니다. 이렇게 하면 소스 데이터 파일을 여러 파일 시스템 간에 배포할 수 있습니다. Platform Server는 데이터 파일을 찾을 때까지 지정한 순서대로 대체 경로를 시도합니다.
