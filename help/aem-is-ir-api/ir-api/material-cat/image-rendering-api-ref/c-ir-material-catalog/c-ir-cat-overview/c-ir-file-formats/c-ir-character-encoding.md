---
description: 이미지 렌더링은 ISO-8859-1 및 UTF-8 인코딩을 사용하는 재료 카탈로그를 지원합니다.
seo-description: 이미지 렌더링은 ISO-8859-1 및 UTF-8 인코딩을 사용하는 재료 카탈로그를 지원합니다.
seo-title: 문자 인코딩
solution: Experience Manager
title: 문자 인코딩
topic: Dynamic Media Image Serving - Image Rendering API
uuid: efc3971b-dca1-4b47-a197-c10270ce17c9
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%

---


# 문자 인코딩{#character-encoding}

이미지 렌더링은 ISO-8859-1 및 UTF-8 인코딩을 사용하는 재료 카탈로그를 지원합니다.

각 파일에 대한 인코딩을 지정하는 데 바이트 순서 표시(BOM)가 사용됩니다. UTF-8의 경우 BOM은 바이트 시퀀스 `EF BB BF`입니다. UTF-8 인코딩은 각 자료 카탈로그 파일의 맨 처음부터 이 문자 시퀀스가 검색될 때 가정합니다. 다른 바이트 시퀀스는 파일이 ISO-8859-1 표준으로 인코딩되는 것으로 해석됩니다.

UTF-8로 구성된 많은 최신 응용 프로그램은 BOM을 자동으로 삽입합니다.
