---
description: searchAssets에서 반환된 메타데이터 필드.
solution: Experience Manager
title: 메타데이터
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 62e3e215-31ea-49fd-937e-d136fdf84aff
TQID: 'https://experienceleague.adobe.com/Cdg9mW2P4YXWlpTiP9ue6cXlFjCByFiw74iJl-sCYNk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 60
ht-degree: 13%

---

# [!DNL Metadata]{#metadata}

searchAssets에서 반환된 메타데이터 필드.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| name | `xsd:string` | 메타데이터 이름. |
| 값 | `xsd:string` | 메타데이터 값. |
| boolVal | `xsd:boolean` | 부울 메타데이터 값(부울 유형 필드만 해당). |
| 롱발 | `xsd:long` | 긴 메타데이터 값(내부 유형 필드에만 해당). |
| doubleVal | `xsd:double` | 이중 메타데이터 값(부동 소수점 형식 필드만 해당). |
| dateVal | `xsd:dateTime` | 날짜 메타데이터 값(날짜 유형 필드에만 해당). |
