---
description: 세미콜론으로 구분된 경로 목록은 상대 파일 경로가 있는 모든 데이터 파일의 루트로 사용됩니다.
seo-description: 세미콜론으로 구분된 경로 목록은 상대 파일 경로가 있는 모든 데이터 파일의 루트로 사용됩니다.
seo-title: 리소스 루트 폴더(ir.resourceRootPaths)
solution: Experience Manager
title: 리소스 루트 폴더(ir.resourceRootPaths)
topic: Dynamic Media Image Serving - Image Rendering API
uuid: a2a8ecd1-ddfe-46c5-bb70-4640e0992de8
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 0%

---


# 리소스 루트 폴더(ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

세미콜론으로 구분된 경로 목록은 상대 파일 경로가 있는 모든 데이터 파일의 루트로 사용됩니다.

절대 경로이거나 *[!DNL install_folder]*&#x200B;에 상대적인 경로일 수 있습니다. 여러 경로를 지정하면 파일이 발견될 때까지 서버가 지정된 순서로 각 루트를 시도합니다. 기본값은 [!DNL ./resources]입니다. 기본 루트 경로는 [!DNL install_folder/resources]입니다.
