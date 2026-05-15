---
description: 레이어 보기 속성.
solution: Experience Manager
title: 레이어 보기 정보
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 25199c86-1df0-41af-b210-e7668a60295e
TQID: 'https://experienceleague.adobe.com/cx-B-BmcEP6vefJY5tsrNMZcwWIKM-pW0CYfP7BjxMM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 46
ht-degree: 13%

---

# [!DNL LayerViewInfo]{#layerviewinfo}

레이어 보기 속성.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| url | `xsd:string` | 템플릿을 나타내는 이미지 서버 URL입니다. `urlModifier` 및 `urlPostAp- plyModifier` 필드를 결합합니다. |
| urlModifier | `xsd:string` | 요청 또는 `urlPostApplyModifier` 명령 전에 적용할 이미지 제공 프로토콜 명령입니다. |
| urlPostApplyModifier | `xsd:string` | `urlModifier` 이후에 적용할 이미지 제공 프로토콜 명령과 요청 명령. |
