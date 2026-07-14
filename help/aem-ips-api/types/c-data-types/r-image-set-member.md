---
description: 이미지 세트에 속하는 Assets입니다.
solution: Experience Manager
title: 이미지 집합 구성원
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: f0857d98-be79-40a6-8a84-c2c7b4c423c5
TQID: 'https://experienceleague.adobe.com/53rc6Cq1i15GdzOpBek7ls7ixq4RN8z0OfZMOZsqYWI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 83717f155466c1b33cab6f1f8830a9fea68c88c5
workflow-type: tm+mt
source-wordcount: 68
ht-degree: 7%

---

# [!DNL ImageSetMember]{#imagesetmember}

이미지 세트에 속하는 Assets입니다.

페이지를 재설정하면 [!DNL eCatalog]이(가) 새 페이지를 시작해야 합니다. `RenderSet`은(는) `RenderSet` 견본의 일부임을 나타냅니다. `eCatalog` 및 `RenderSet` 집합에 대해 값이 `true`(으)로 강제 설정됩니다.

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| asset | `type:Asset` | 이미지 세트 배열의 Assets. |
| pageReset | `xsd:boolean` | 새 페이지를 시작합니다. 설정이 무시되고 `eCatalog` 및 `RenderSet` 집합에 대해 값이 `true`(으)로 강제 적용됩니다. |

