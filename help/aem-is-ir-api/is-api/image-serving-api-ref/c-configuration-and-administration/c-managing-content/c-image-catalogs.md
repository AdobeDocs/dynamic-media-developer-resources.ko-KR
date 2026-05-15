---
description: 이미지 카탈로그는 글꼴, ICC 프로파일, 명령 매크로뿐만 아니라 다양한 서버 구성 설정을 제공합니다.
solution: Experience Manager
title: 이미지 카탈로그
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 70ec4566-a937-464e-8219-b7eda3ab66c1
TQID: 'https://experienceleague.adobe.com/kfojwk0K5RfRtZdxJmdojqsLirnP6LoXbtFRJ5272lg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 112
ht-degree: 0%

---

# 이미지 카탈로그{#image-catalogs}

이미지 카탈로그는 글꼴, ICC 프로파일, 명령 매크로뿐만 아니라 다양한 서버 구성 설정을 제공합니다.

요청에 사용되는 이미지 및 정적 콘텐츠 ID를 실제 파일 경로에 매핑하고, 이미지 맵과 같은 다양한 이미지 메타데이터를 저장하고, 템플릿 및 이미지 세트에 대한 컨테이너를 제공합니다.

이미지 카탈로그는 [!DNL Platform Server]에서만 액세스하며 이미지 서버에서는 액세스하지 않습니다. 카탈로그 특성 파일에는 .ini 접미사가 있어야 하며 [!DNL Platform Server]의 카탈로그 폴더( `PS::CatalogFolder`)에 있어야 합니다. 최소한 기본 이미지 카탈로그가 필요하며 [!DNL Platform Server]이(가) 올바르게 작동하려면 모든 특성으로 채워야 합니다.
