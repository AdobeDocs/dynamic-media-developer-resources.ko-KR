---
description: 레이어 보기 속성입니다.
solution: Experience Manager
title: LayerViewInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 11%

---


# LayerViewInfo{#layerviewinfo}

레이어 보기 속성입니다.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| `*`url`*` | `xsd:string` | 템플릿을 나타내는 이미지 서버 URL. `urlModifier` 및 `urlPostAp- plyModifier` 필드를 결합합니다. |
| `*`urlModifier`*` | `xsd:string` | 이미지 제공 프로토콜 명령을 요청 또는 `urlPostApplyModifier` 명령 전에 적용합니다. |
| `*`urlPostApplyModifier`*` | `xsd:string` | `urlModifier` 뒤에 적용할 이미지 제공 프로토콜 명령 및 요청 명령 |

