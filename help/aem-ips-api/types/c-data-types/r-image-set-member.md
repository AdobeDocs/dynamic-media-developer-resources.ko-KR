---
description: 이미지 세트에 속하는 Assets입니다.
solution: Experience Manager
title: 이미지 집합 구성원
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: f0857d98-be79-40a6-8a84-c2c7b4c423c5
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 7%

---

# [!DNL ImageSetMember]{#imagesetmember}

이미지 세트에 속하는 Assets입니다.

페이지를 재설정하면 [!DNL eCatalog]이(가) 새 페이지를 시작해야 합니다. `RenderSet`은(는) `RenderSet` 견본의 일부임을 나타냅니다. `true` 및 `eCatalog` 집합에 대해 값이 `RenderSet`(으)로 강제 설정됩니다.

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| asset | `type:Asset` | 이미지 세트 배열의 Assets. |
| pageReset | `xsd:boolean` | 새 페이지를 시작합니다. 설정이 무시되고 `true` 및 `eCatalog` 집합에 대해 값이 `RenderSet`(으)로 강제 적용됩니다. |
