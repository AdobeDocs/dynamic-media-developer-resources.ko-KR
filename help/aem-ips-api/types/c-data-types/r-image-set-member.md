---
description: 이미지 세트에 속하는 자산입니다.
seo-description: 이미지 세트에 속하는 자산입니다.
seo-title: ImageSetMember
solution: Experience Manager
title: ImageSetMember
topic: Scene7 Image Production System API
uuid: bd013609-aed7-4c85-80f9-16be7fce99a3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ImageSetMember{#imagesetmember}

이미지 세트에 속하는 자산입니다.

페이지 재설정은 새 페이지를 [!DNL eCatalog] 시작해야 함을 의미합니다. `RenderSet` 는 견본의 일부임을 `RenderSet` 나타냅니다. 값은 `true` 및 `eCatalog` `RenderSet` 세트에 대해 강제로 지정됩니다.

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| ` *`asset`*` | `type:Asset` | 이미지 집합 배열의 자산입니다. |
| ` *`pageReset`*` | `xsd:boolean` | 새 페이지를 시작합니다. 설정이 무시되고 `true` 및 `eCatalog` `RenderSet` 세트에 대해 값이 강제로 지정됩니다. |

