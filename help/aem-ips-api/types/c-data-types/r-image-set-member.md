---
description: 이미지 세트에 속하는 자산.
solution: Experience Manager
title: ImageSetMember
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: f0857d98-be79-40a6-8a84-c2c7b4c423c5
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 7%

---

# ImageSetMember{#imagesetmember}

이미지 세트에 속하는 자산.

페이지 재설정은 [!DNL eCatalog] 새 페이지를 시작해야 합니다. `RenderSet` 는 해당 항목이 `RenderSet` 견본. 값은 `true` 대상 `eCatalog` 및 `RenderSet` 를 설정합니다.

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| asset | `type:Asset` | 이미지 세트 배열의 자산. |
| pageReset | `xsd:boolean` | 새 페이지를 시작합니다. 설정은 무시되고 값은 강제로 `true` 대상 `eCatalog` 및 `RenderSet` 를 설정합니다. |
