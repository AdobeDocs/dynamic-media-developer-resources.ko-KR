---
description: 검색 결과에서 제외할 생성 엔진 및 생성된 에셋 유형을 결정합니다.
solution: Experience Manager
title: ExcludeVasputeCondition
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 5b37e01b-9e9c-4d34-9d39-1f9bfe356e53
TQID: 'https://experienceleague.adobe.com/PwNBhs403st6NxlKBVOgJJ1qhQuxyJglDJPC-UEGyJw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 56
ht-degree: 8%

---

# [!DNL ExcludeByproductCondition]{#excludebyproductcondition}

검색 결과에서 제외할 생성 엔진 및 생성된 에셋 유형을 결정합니다.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| [!DNL engine] | `xsd:string` | 제외할 자산을 만든 생성 엔진입니다. 값에 대해서는 생성 정보 를 참조하십시오. |
| generatedAssetType | `xsd:string` | 제외된 자산 유형. 값에 대해서는 자산 유형 을 참조하십시오. |
