---
description: ICC 프로파일 속성에 대한 정보를 업데이트합니다.
solution: Experience Manager
title: IccProfileFieldUpdate
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b988a430-8ed6-456b-b37b-b4185c5d3b32
TQID: 'https://experienceleague.adobe.com/-HbYlEjS3SdM9Sr0jgaQdve1H9wr7e51oAvAy-C-0vI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 52
ht-degree: 9%

---

# [!DNL IccProfileFieldUpdate]{#iccprofilefieldupdate}

ICC 프로파일 속성에 대한 정보를 업데이트합니다.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| assetHandle | `xsd:string` | 업데이트할 ICC 프로파일 자산의 핸들입니다. |
| [!DNL class] | `xsd:string` | 프로필 클래스(값은 &quot;프로필 클래스&quot; 참조) |
| 색상 공간 | `xsd:string` | 프로필 색상 공간(값은 &quot;색상 공간&quot; 참조). |
| pcsType | `xsd:string` | 프로필 연결 공간(값은 &quot;색상 공간&quot; 참조). |
