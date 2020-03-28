---
description: 정적 컨텐츠 소스 데이터 파일은 플랫폼 서버에서만 액세스할 수 있습니다.
seo-description: 정적 컨텐츠 소스 데이터 파일은 플랫폼 서버에서만 액세스할 수 있습니다.
seo-title: 정적 컨텐츠 소스 데이터
solution: Experience Manager
title: 정적 컨텐츠 소스 데이터
topic: Scene7 Image Serving - Image Rendering API
uuid: a3280ce7-20d7-4f4b-bf3e-e77cc7aca35f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 정적 컨텐츠 소스 데이터{#static-content-source-data}

정적 컨텐츠 소스 데이터 파일은 플랫폼 서버에서만 액세스할 수 있습니다.

정적 컨텐츠 데이터 파일의 경로는 다음과 같이 결정됩니다.

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

서버는 절대 파일 경로가 설정될 때까지 경로 세그먼트를 오른쪽에서 왼쪽으로 결합합니다.

모든 ` *[!DNL rootPath]*` 세그먼트는 비어 있거나 상대 또는 절대 경로 세그먼트일 수 있습니다.

` *[!DNL catalogPath]*` 은 절대 또는 상대 파일 경로/이름입니다. *[!DNL requestPath]* 는 상대 파일 경로/이름이어야 합니다.

여러 `PS::staticContent.rootPaths` 값을 에서 정의할 수 있습니다 [!DNL PlatformServer.conf]. 이를 통해 소스 데이터 파일을 여러 파일 시스템에 배포할 수 있습니다. 플랫폼 서버는 데이터 파일을 찾을 때까지 지정된 순서대로 대체 경로를 시도합니다.
