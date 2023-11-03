---
description: 정적 콘텐츠 소스 데이터 파일은 [!DNL Platform Server].
solution: Experience Manager
title: 정적 콘텐츠 소스 데이터
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 3cf01fc2-c925-4039-8e03-cb909cca6a51
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---

# 정적 콘텐츠 소스 데이터{#static-content-source-data}

정적 콘텐츠 소스 데이터 파일은 [!DNL Platform Server].

정적 콘텐츠 데이터 파일의 경로는 다음과 같이 확인됩니다.

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

서버는 절대 파일 경로가 설정될 때까지 경로 세그먼트를 오른쪽에서 왼쪽으로 결합합니다.

모두 ` *[!DNL rootPath]*` 세그먼트는 비어 있거나 상대 또는 절대 경로 세그먼트일 수 있습니다.

` *[!DNL catalogPath]*` 는 절대 또는 상대 파일 경로/이름입니다. *[!DNL requestPath]* 상대 파일 경로/이름이어야 합니다.

복수 `PS::staticContent.rootPaths` 값은 다음에서 정의할 수 있습니다. [!DNL PlatformServer.conf]. 이를 통해 소스 데이터 파일을 여러 파일 시스템에 분산할 수 있습니다. 다음 [!DNL Platform Server] 데이터 파일이 발견될 때까지 지정된 순서대로 대체 경로를 시도합니다.
