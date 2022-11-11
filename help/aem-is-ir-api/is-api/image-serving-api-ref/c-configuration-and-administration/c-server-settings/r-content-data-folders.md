---
description: 컨텐츠 데이터 폴더에 대해 이러한 서버 설정을 사용합니다.
solution: Experience Manager
title: 컨텐츠 데이터 폴더
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 9aa4121f-25f8-49d0-a304-7ae756c046f5
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---

# 컨텐츠 데이터 폴더{#content-data-folders}

컨텐츠 데이터 폴더에 대해 이러한 서버 설정을 사용합니다.

## IS::RootPath - 이미지 데이터 루트 폴더 {#section-5c57569514bb4d00b19de31d2e137e3b}

이미지, 글꼴 및 ICC 프로파일을 포함한 모든 소스 데이터의 위치입니다. 이 경로는 *[!DNL install_folder]*: 세미콜론으로 구분됩니다. 비어 있으면, *[!DNL install_folder]* 는 기본 루트입니다. 여러 파일 시스템에 이미지 데이터를 배포하도록 여러 값을 지정할 수 있습니다. 이미지 서버는 요청된 파일을 찾을 때까지 지정된 순서대로 루트 경로를 시도합니다.

## PS::staticContent.rootPath - 정적 컨텐츠 데이터 루트 폴더 {#section-a4f5b6942b7b4abdbf825b1f2e932cfe}

를 통해 전달하려는 정적 콘텐츠 소스 데이터의 위치입니다 [!DNL /is/static] 컨텍스트. 에 상대적인 하나 이상의 절대 파일 경로나 경로일 수 있습니다 *[!DNL install_folder]*: 세미콜론으로 구분됩니다. 비어 있으면, *[!DNL install_folder]* 는 기본 루트입니다.

여러 파일 시스템에 정적 콘텐츠를 배포하기 위해 여러 값을 세미콜론으로 구분하여 지정할 수 있습니다. 일반적으로 와 동일한 값으로 설정됩니다 `IS::RootPath`.

다음 [!DNL Platform Server] 요청된 파일이 발견될 때까지 지정된 순서대로 루트 경로를 시도합니다.

>[!NOTE]
>
>기본적으로 이 필드는 의도적으로 존재하지 않는 위치( [!DNL *[!DNL install_folder]*/static]))을 설정하는 것이 좋습니다.

## IS::SaveDirectory - 파일 저장 루트 폴더 {#section-1c517f8d49ce4cb8b9013e520bf309c9}

의 루트 경로 `attribute::SavePath` (다음 사용) `req=saveToFile`). 이미지 서버는 이미지 파일을 만들 하위 폴더에 대한 액세스 권한을 만들 수 있어야 합니다.
