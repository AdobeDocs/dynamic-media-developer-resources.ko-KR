---
description: 이미지 제공은 ISO-8859-1 및 UTF-8 인코딩을 사용하는 이미지 카탈로그를 지원합니다.
solution: Experience Manager
title: 문자 인코딩
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e6e50c2a-53d3-4776-a3f6-4a9d3407e562
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---

# 문자 인코딩{#character-encoding}

이미지 제공은 ISO-8859-1 및 UTF-8 인코딩을 사용하는 이미지 카탈로그를 지원합니다.

BOM(바이트 순서 표시)을 사용하여 각 파일의 인코딩을 지정합니다. UTF-8의 경우 BOM은 바이트 시퀀스입니다 `EF BB BF`. 이 문자 시퀀스가 각 이미지 카탈로그 파일의 맨 처음에 감지되면 UTF-8 인코딩이 적용됩니다. 다른 바이트 시퀀스를 사용하면 파일이 ISO-8859-1 표준으로 인코딩되는 것으로 해석됩니다.

대부분의 최신 응용 프로그램은 UTF-8로 구성된 경우 BOM을 자동으로 삽입합니다.
