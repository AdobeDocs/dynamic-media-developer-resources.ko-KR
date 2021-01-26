---
description: 콘텐트 데이터 폴더에 대해 다음 서버 설정을 사용합니다.
seo-description: 콘텐트 데이터 폴더에 대해 다음 서버 설정을 사용합니다.
seo-title: 콘텐트 데이터 폴더
solution: Experience Manager
title: 콘텐트 데이터 폴더
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 7c4d60ca-8a8b-453c-887d-a6a16eacc883
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---


# 콘텐트 데이터 폴더{#content-data-folders}

콘텐트 데이터 폴더에 대해 다음 서버 설정을 사용합니다.

## IS::RootPath - 이미지 데이터 루트 폴더 {#section-5c57569514bb4d00b19de31d2e137e3b}

이미지, 글꼴 및 ICC 프로필을 비롯한 모든 소스 데이터의 위치입니다. 이 경로는 *[!DNL install_folder]*&#x200B;에 상대적인 하나 이상의 절대 파일 경로 또는 경로이며 세미콜론으로 구분됩니다. 비어 있으면 *[!DNL install_folder]*&#x200B;이(가) 기본 루트입니다. 여러 파일 시스템에 이미지 데이터를 배포하도록 여러 값을 지정할 수 있습니다. 이미지 서버는 요청된 파일을 찾을 때까지 지정된 순서대로 루트 경로를 시도합니다.

## PS::staticContent.rootPath - 정적 컨텐츠 데이터 루트 폴더 {#section-a4f5b6942b7b4abdbf825b1f2e932cfe}

[!DNL /is/static] 컨텍스트를 통해 전달하려는 정적 컨텐츠 소스 데이터의 위치입니다. *[!DNL install_folder]*&#x200B;에 상대적인 하나 이상의 절대 파일 경로 또는 경로가 세미콜론으로 구분될 수 있습니다. 비어 있으면 *[!DNL install_folder]*&#x200B;이(가) 기본 루트입니다.

여러 개의 값을 세미콜론으로 구분하여 여러 파일 시스템에 정적 컨텐츠를 배포할 수 있습니다. 일반적으로 `IS::RootPath`과 동일한 값으로 설정됩니다.

플랫폼 서버는 요청된 파일을 찾을 때까지 지정된 순서대로 루트 경로를 시도합니다.

>[!NOTE]
>
>기본적으로 이 필드는 존재하지 않는 위치( [!DNL *[!DNL install_folder]*/static])로 설정되므로 정적 콘텐츠 서비스를 효과적으로 비활성화할 수 있습니다.

## IS::SaveDirectory - 파일 저장 루트 폴더 {#section-1c517f8d49ce4cb8b9013e520bf309c9}

`attribute::SavePath`(`req=saveToFile`에서 사용)의 루트 경로입니다. 이미지 서버가 이미지 파일을 만들 하위 폴더에 대한 만들기 액세스 권한을 가져야 합니다.
