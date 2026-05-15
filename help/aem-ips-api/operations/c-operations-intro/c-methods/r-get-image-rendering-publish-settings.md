---
description: 내부 전용입니다. 이미지 렌더링 재질 카탈로그 참조-카탈로그 속성 섹션을 참조하십시오.
solution: Experience Manager
title: getImageRenderingPublishSettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 152dfd61-2fba-47b4-8e69-fbbc8fb57f87
TQID: 'https://experienceleague.adobe.com/-zBv9N9COcH6KjyHfgjYF4TXblntNiZMVBB6nr-oe2w'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 76
ht-degree: 17%

---

# getImageRenderingPublishSettings{#getimagerenderingpublishsettings}

내부 전용입니다. 이미지 렌더링 재질 카탈로그 참조-카탈로그 속성 섹션을 참조하십시오.

구문

## 승인된 사용자 유형 {#section-1097e0563c61480a8e97822dc3527070}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-4f2cb8c589384816bb2525654ec49963}

**입력(getImageRenderingPublishSettingsParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 이미지 렌더링 게시 설정을 가져오려는 회사에 대한 핸들입니다. |
| context핸들 | `xsd:string` | 예 | 게시 컨텍스트에 대한 핸들입니다. |

**출력(getImageRenderingPublishSettingsReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| publishSettingsArray | `type:ConfigSettingArray` | 예 | 이미지 렌더링 게시 설정입니다. |
