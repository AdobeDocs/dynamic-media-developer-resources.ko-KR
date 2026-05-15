---
title: 문자 인코딩
description: 이미지 렌더링은 ISO-8859-1 및 UTF-8 인코딩을 사용하는 재질 카탈로그를 지원합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ee7b33fd-7607-4bff-867b-6e7a837a9ed4
TQID: 'https://experienceleague.adobe.com/1ITLimvCUD8hrdfeyyod6nE0sMmfIJ3ySx5HCFa2ZQk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 104
ht-degree: 0%

---

# 문자 인코딩{#character-encoding}

이미지 렌더링은 ISO-8859-1 및 UTF-8 인코딩을 사용하는 재질 카탈로그를 지원합니다.

BOM(바이트 순서 표시)을 사용하여 각 파일의 인코딩을 지정합니다. UTF-8의 경우 BOM은 바이트 시퀀스 `EF BB BF`입니다. 이 문자 시퀀스가 각 재질 카탈로그 파일의 맨 처음에 감지되면 UTF-8 인코딩이 적용됩니다. 다른 모든 바이트 시퀀스를 사용하면 파일이 ISO-8859-1 표준으로 인코딩되는 것으로 해석됩니다.

대부분의 최신 응용 프로그램은 UTF-8로 구성된 경우 BOM을 자동으로 삽입합니다.
