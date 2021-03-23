---
description: 이미지 세트에 속하는 자산입니다.
seo-description: 이미지 세트에 속하는 자산입니다.
seo-title: ImageSetMember
solution: Experience Manager
title: ImageSetMember
uuid: bd013609-aed7-4c85-80f9-16be7fce99a3
feature: Dynamic Media Classic,SDK/API,이미지 세트
role: 개발자,관리자
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 5%

---


# ImageSetMember{#imagesetmember}

이미지 세트에 속하는 자산입니다.

페이지 재설정은 [!DNL eCatalog]이(가) 새 페이지를 시작해야 함을 의미합니다. `RenderSet` 견본의 일부임을  `RenderSet` 나타냅니다. 값은 `eCatalog` 및 `RenderSet` 세트에 대해 `true`에 강제 적용됩니다.

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| `*`asset`*` | `type:Asset` | 이미지 집합 배열의 에셋입니다. |
| `*`pageReset`*` | `xsd:boolean` | 새 페이지를 시작합니다. 설정이 무시되고 값이 `eCatalog` 및 `RenderSet` 집합에 대해 `true`에 강제 적용됩니다. |

