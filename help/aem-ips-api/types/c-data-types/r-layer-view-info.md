---
description: 레이어 보기 속성을 참조하십시오.
seo-description: 레이어 보기 속성을 참조하십시오.
seo-title: LayerViewInfo
solution: Experience Manager
title: LayerViewInfo
topic: Scene7 Image Production System API
uuid: 58d26f4d-03a6-4f57-bc8e-117355c0d74c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# LayerViewInfo{#layerviewinfo}

레이어 보기 속성을 참조하십시오.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| ` *`url`*` | `xsd:string` | 템플릿을 나타내는 이미지 서버 URL. 결합 `urlModifier` 및 `urlPostAp- plyModifier` 필드 |
| ` *`urlModifier`*` | `xsd:string` | 요청이나 `urlPostApplyModifier` 명령 전에 적용할 이미지 제공 프로토콜 명령 |
| ` *`urlPostApplyModifier`*` | `xsd:string` | Image serving protocol command to apply after `urlModifier` and request commands. |

