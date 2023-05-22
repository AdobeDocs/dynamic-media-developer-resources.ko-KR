---
description: 세미콜론으로 구분된 경로 목록은 상대 파일 경로가 있는 모든 데이터 파일의 루트 역할을 합니다.
solution: Experience Manager
title: 리소스 루트 폴더(ir.resourceRootPaths)
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 49fd45da-1af9-4016-8fc6-6ec17b7e553b
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 0%

---

# 리소스 루트 폴더(ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

세미콜론으로 구분된 경로 목록은 상대 파일 경로가 있는 모든 데이터 파일의 루트 역할을 합니다.

절대 경로이거나 상대 경로일 수 있습니다. *[!DNL install_folder]*. 여러 경로를 지정하면 파일이 발견될 때까지 서버는 주어진 순서로 각 루트를 시도합니다. 기본값은 입니다 [!DNL ./resources]의 기본 루트 경로용 [!DNL install_folder/resources].
