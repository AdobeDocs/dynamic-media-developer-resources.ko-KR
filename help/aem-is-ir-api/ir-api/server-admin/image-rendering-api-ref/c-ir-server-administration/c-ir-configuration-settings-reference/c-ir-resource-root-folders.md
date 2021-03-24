---
description: 세미콜론으로 구분된 경로 목록은 상대 파일 경로가 있는 모든 데이터 파일의 루트로 사용됩니다.
solution: Experience Manager
title: 리소스 루트 폴더(ir.resourceRootPaths)
feature: Dynamic Media Classic,SDK/API
role: 개발자,관리자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 0%

---


# 리소스 루트 폴더(ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

세미콜론으로 구분된 경로 목록은 상대 파일 경로가 있는 모든 데이터 파일의 루트로 사용됩니다.

절대 경로이거나 *[!DNL install_folder]*&#x200B;에 상대적인 경로일 수 있습니다. 여러 경로가 지정된 경우 해당 파일을 찾을 때까지 서버가 지정된 순서대로 각 루트를 시도합니다. 기본값은 [!DNL ./resources]입니다. 기본 루트 경로는 [!DNL install_folder/resources]입니다.
