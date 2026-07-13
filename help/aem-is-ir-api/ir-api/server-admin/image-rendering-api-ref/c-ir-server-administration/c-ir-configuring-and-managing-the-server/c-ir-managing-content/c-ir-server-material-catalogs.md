---
description: 재질 카탈로그는 많은 이미지 렌더링 구성 설정을 제공합니다.
solution: Experience Manager
title: 자료 카탈로그
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c0b030b7-bcfb-4e6d-b74a-4533bdb801bf
TQID: 'https://experienceleague.adobe.com/FOwuQrKYaRJ78mdRbPeoy71crT9GHj4R5MXFbMGnrZE'
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
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 108
ht-degree: 0%

---

# 자료 카탈로그{#material-catalogs}

재질 카탈로그는 많은 이미지 렌더링 구성 설정을 제공합니다.

재질 카탈로그는 요청에 사용된 비네팅 및 재질 ID를 실제 파일 경로에 매핑하고, 자료와 관련된 모든 메타데이터를 저장하고, 템플릿에 대한 컨테이너를 제공할 수 있습니다. ICC 프로파일 및 명령 매크로를 추적합니다.

재질 카탈로그는 [!DNL Platform Server]과(와) 함께 위치한 이미지 렌더링의 Java 구성 요소에서만 액세스됩니다. 카탈로그 특성 파일은 [!DNL .ini] 접미사를 사용하고 등록된 카탈로그 폴더([ir.catalogRootPath](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-catalog-folder.md#concept-1c1d308112054bb99e3895c3fb8ca5f7))에 배치해야 합니다. 기본 재질 카탈로그([!DNL default.ini])는 항상 있어야 하며 이미지 제공의 올바른 작동을 위해 모든 특성으로 채워야 합니다.

