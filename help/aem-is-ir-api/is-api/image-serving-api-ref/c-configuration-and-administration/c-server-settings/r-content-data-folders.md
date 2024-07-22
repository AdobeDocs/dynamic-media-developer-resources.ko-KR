---
description: 컨텐츠 데이터 폴더에 대해 이러한 서버 설정을 사용합니다.
solution: Experience Manager
title: 컨텐츠 데이터 폴더
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 9aa4121f-25f8-49d0-a304-7ae756c046f5
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---

# 컨텐츠 데이터 폴더{#content-data-folders}

컨텐츠 데이터 폴더에 대해 이러한 서버 설정을 사용합니다.

## IS::RootPath - 이미지 데이터 루트 폴더 {#section-5c57569514bb4d00b19de31d2e137e3b}

이미지, 글꼴 및 ICC 프로파일을 포함한 모든 소스 데이터의 위치. 하나 이상의 절대 파일 경로이거나 *[!DNL install_folder]*&#x200B;에 상대적인 경로이며 세미콜론으로 구분됩니다. 비어 있으면 *[!DNL install_folder]*&#x200B;이(가) 기본 루트입니다. 여러 값을 지정하여 여러 파일 시스템에 이미지 데이터를 배포할 수 있습니다. 이미지 서버는 요청된 파일을 찾을 때까지 지정된 순서대로 루트 경로를 시도합니다.

## PS::staticContent.rootPath - 정적 컨텐츠 데이터 루트 폴더 {#section-a4f5b6942b7b4abdbf825b1f2e932cfe}

[!DNL /is/static] 컨텍스트를 통해 전달하려는 정적 콘텐츠 원본 데이터의 위치입니다. 하나 이상의 절대 파일 경로이거나 *[!DNL install_folder]*&#x200B;을(를) 기준으로 세미콜론으로 구분된 경로일 수 있습니다. 비어 있으면 *[!DNL install_folder]*&#x200B;이(가) 기본 루트입니다.

여러 값을 세미콜론으로 구분하여 지정하여 정적 콘텐츠를 여러 파일 시스템에 배포할 수 있습니다. 일반적으로 `IS::RootPath`과(와) 동일한 값으로 설정됩니다.

[!DNL Platform Server]은(는) 요청된 파일을 찾을 때까지 지정된 순서대로 루트 경로를 시도합니다.

>[!NOTE]
>
>기본적으로 이 필드는 의도적으로 존재하지 않는 위치([!DNL *[!DNL install_folder]*/static])로 설정되어 정적 콘텐츠 서비스를 효과적으로 비활성화합니다.

## IS::SaveDirectory - 파일 루트 폴더 저장 {#section-1c517f8d49ce4cb8b9013e520bf309c9}

`attribute::SavePath`의 루트 경로(`req=saveToFile`에서 사용). 이미지 서버는 이미지 파일을 만드는 하위 폴더에 대해 만들기 액세스 권한이 있어야 합니다.
