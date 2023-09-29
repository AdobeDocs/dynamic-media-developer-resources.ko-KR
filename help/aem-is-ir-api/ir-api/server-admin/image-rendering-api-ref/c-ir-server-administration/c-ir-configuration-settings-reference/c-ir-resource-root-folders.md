---
title: 리소스 루트 폴더(ir.resourceRootPaths)
description: 세미콜론으로 구분된 경로 목록은 상대 파일 경로가 있는 모든 데이터 파일의 루트 역할을 합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 49fd45da-1af9-4016-8fc6-6ec17b7e553b
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 0%

---

# 리소스 루트 폴더(ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

세미콜론으로 구분된 경로 목록은 상대 파일 경로가 있는 모든 데이터 파일의 루트 역할을 합니다.

절대 경로이거나 상대 경로일 수 있습니다. *[!DNL install_folder]*. 여러 경로를 지정한 경우 서버는 파일을 찾을 때까지 주어진 순서로 각 루트를 시도합니다. 기본값은 입니다 [!DNL ./resources]의 기본 루트 경로용 [!DNL install_folder/resources].
