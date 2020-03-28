---
description: 콘텐트 데이터 폴더에 대해 이러한 서버 설정을 사용합니다.
seo-description: 콘텐트 데이터 폴더에 대해 이러한 서버 설정을 사용합니다.
seo-title: 콘텐트 데이터 폴더
solution: Experience Manager
title: 콘텐트 데이터 폴더
topic: Scene7 Image Serving - Image Rendering API
uuid: 7c4d60ca-8a8b-453c-887d-a6a16eacc883
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 콘텐트 데이터 폴더{#content-data-folders}

콘텐트 데이터 폴더에 대해 이러한 서버 설정을 사용합니다.

## IS::RootPath - 이미지 데이터 루트 폴더 {#section-5c57569514bb4d00b19de31d2e137e3b}

이미지, 글꼴, ICC 프로파일 등 모든 소스 데이터의 위치입니다. 이 경로는 세미콜론으로 구분된 하나 이상의 절대 파일 경로 또는 상대 경로일 *[!DNL install_folder]*&#x200B;수 있습니다. 비어 있으면 기본 *[!DNL install_folder]* 루트가 됩니다. 여러 파일 시스템에 이미지 데이터를 배포하도록 여러 값을 지정할 수 있습니다. 이미지 서버는 요청된 파일을 찾을 때까지 지정된 순서대로 루트 경로를 시도합니다.

## PS::staticContent.rootPath - 정적 컨텐츠 데이터 루트 폴더 {#section-a4f5b6942b7b4abdbf825b1f2e932cfe}

컨텍스트를 통해 전달하려는 정적 컨텐츠 소스 데이터의 위치입니다. [!DNL /is/static] 하나 이상의 절대 파일 경로 또는 상대 경로를 세미콜론으로 *[!DNL install_folder]*&#x200B;구분하여 사용할 수 있습니다. 비어 있으면 기본 *[!DNL install_folder]* 루트가 됩니다.

여러 값을 세미콜론으로 구분하여 여러 파일 시스템에 정적 컨텐츠를 배포할 수 있습니다. 일반적으로 동일한 값으로 `IS::RootPath`설정됩니다.

플랫폼 서버는 요청된 파일을 찾을 때까지 지정된 순서대로 루트 경로를 시도합니다.

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>기본적으로 이 필드는 존재하지 않는 위치( [!DNL/ *[!DNL install_folder]* static])로 설정되므로 정적 콘텐츠 서비스를 효과적으로 비활성화할 수 있습니다.

## IS::SaveDirectory - 파일 저장 루트 폴더 {#section-1c517f8d49ce4cb8b9013e520bf309c9}

의 루트 경로 `attribute::SavePath` (사용 `req=saveToFile`). 이미지 서버에는 이미지 파일을 만들 하위 폴더에 대한 만들기 액세스 권한이 있어야 합니다.
