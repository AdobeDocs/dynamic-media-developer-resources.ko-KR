---
description: 정적 콘텐츠 원본 데이터 파일은  [!DNL Platform Server]에서만 액세스합니다.
solution: Experience Manager
title: 정적 콘텐츠 소스 데이터
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 3cf01fc2-c925-4039-8e03-cb909cca6a51
TQID: 'https://experienceleague.adobe.com/XFhKuqGPsarkFZcYcBo7XuyCEsiJINf-o6koIZQKAXU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 112
ht-degree: 0%

---

# 정적 콘텐츠 소스 데이터{#static-content-source-data}

정적 콘텐츠 원본 데이터 파일은 [!DNL Platform Server]에서만 액세스할 수 있습니다.

정적 콘텐츠 데이터 파일의 경로는 다음과 같이 확인됩니다.

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

서버는 절대 파일 경로가 설정될 때까지 경로 세그먼트를 오른쪽에서 왼쪽으로 결합합니다.

모든 ` *[!DNL rootPath]*` 세그먼트는 비어 있거나 상대 또는 절대 경로 세그먼트일 수 있습니다.

` *[!DNL catalogPath]*`은(는) 절대 또는 상대 파일 경로/이름입니다. *[!DNL requestPath]*&#x200B;은(는) 상대 파일 경로/이름이어야 합니다.

[!DNL PlatformServer.conf]에서 여러 `PS::staticContent.rootPaths` 값을 정의할 수 있습니다. 이를 통해 소스 데이터 파일을 여러 파일 시스템에 분산할 수 있습니다. [!DNL Platform Server]은(는) 데이터 파일을 찾을 때까지 지정된 순서대로 대체 경로를 시도합니다.
