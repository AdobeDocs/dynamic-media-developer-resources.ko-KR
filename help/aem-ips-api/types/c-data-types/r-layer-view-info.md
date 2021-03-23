---
description: 레이어 보기 속성입니다.
seo-description: 레이어 보기 속성입니다.
seo-title: LayerViewInfo
solution: Experience Manager
title: LayerViewInfo
uuid: 58d26f4d-03a6-4f57-bc8e-117355c0d74c
feature: Dynamic Media Classic,SDK/API
role: 개발자,관리자
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 10%

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

