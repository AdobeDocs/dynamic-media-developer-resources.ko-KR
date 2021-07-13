---
description: 이미지 제공 서비스는 ISO-8859-1 및 UTF-8 인코딩을 사용하여 이미지 카탈로그를 지원합니다.
solution: Experience Manager
title: 문자 인코딩
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e6e50c2a-53d3-4776-a3f6-4a9d3407e562
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 0%

---

# 문자 인코딩{#character-encoding}

이미지 제공 서비스는 ISO-8859-1 및 UTF-8 인코딩을 사용하여 이미지 카탈로그를 지원합니다.

각 파일에 대한 인코딩을 지정하는 데 바이트 순서 표시(BOM)가 사용됩니다. UTF-8의 경우 BOM은 바이트 시퀀스 `EF BB BF`입니다. UTF-8 인코딩은 각 이미지 카탈로그 파일의 시작 부분에서 이 문자 시퀀스가 검색될 때 가정합니다. 다른 바이트 시퀀스는 파일이 ISO-8859-1 표준으로 인코딩되는 것으로 해석됩니다.

UTF-8에 대해 구성된 대부분의 일반 응용 프로그램에서 BOM을 자동으로 삽입합니다.
