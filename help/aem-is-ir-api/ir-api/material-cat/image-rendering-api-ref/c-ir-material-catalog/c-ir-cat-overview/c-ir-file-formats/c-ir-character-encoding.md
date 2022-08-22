---
title: 문자 인코딩
description: 이미지 렌더링은 ISO-8859-1 및 UTF-8 인코딩을 사용하는 자료 카탈로그를 지원합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ee7b33fd-7607-4bff-867b-6e7a837a9ed4
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---

# 문자 인코딩{#character-encoding}

이미지 렌더링은 ISO-8859-1 및 UTF-8 인코딩을 사용하는 자료 카탈로그를 지원합니다.

각 파일에 대한 인코딩을 지정하는 데 바이트 순서 표시(BOM)가 사용됩니다. UTF-8의 경우 BOM은 바이트 시퀀스입니다 `EF BB BF`. UTF-8 인코딩은 각 재료 카탈로그 파일의 맨 시작 부분에서 이 문자 시퀀스가 검색될 때 가정합니다. 다른 바이트 시퀀스는 파일이 ISO-8859-1 표준으로 인코딩되는 것으로 해석됩니다.

UTF-8에 대해 구성된 경우 BOM을 자동으로 삽입합니다.
