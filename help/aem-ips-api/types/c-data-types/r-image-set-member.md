---
description: 이미지 세트에 속하는 자산.
solution: Experience Manager
title: ImageSetMember
feature: Dynamic Media Classic,SDK/API,이미지 세트
role: Developer,Administrator
exl-id: f0857d98-be79-40a6-8a84-c2c7b4c423c5
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 6%

---

# ImageSetMember{#imagesetmember}

이미지 세트에 속하는 자산.

페이지 재설정은 [!DNL eCatalog]이(가) 새 페이지를 시작해야 함을 의미합니다. `RenderSet` 견본의 일부임을  `RenderSet` 나타냅니다. 값은 `eCatalog` 및 `RenderSet` 집합에 대해 `true`로 강제 설정됩니다.

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| `*`asset`*` | `type:Asset` | 이미지 세트 배열의 자산. |
| `*`pageReset`*` | `xsd:boolean` | 새 페이지를 시작합니다. 설정이 무시되고 `eCatalog` 및 `RenderSet` 집합에 대해 값이 `true`에 강제 설정됩니다. |
