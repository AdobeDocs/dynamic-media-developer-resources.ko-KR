---
description: PostScript 파일 속성입니다.
seo-description: PostScript 파일 속성입니다.
seo-title: GenerationInfo
solution: Experience Manager
title: GenerationInfo
topic: Scene7 Image Production System API
uuid: 166637e5-b981-4f64-8d92-5fce4f1b20d2
translation-type: tm+mt
source-git-commit: 55015831ed1971a305ddbd8085c95626507355e0
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 13%

---


# GenerationInfo{#generationinfo}

PostScript 파일 속성입니다.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| ` *`엔진`*` | `xsd:string` | 사용되는 생성 엔진(값에 대한 &quot;생성 정보&quot; 참조). |
| ` *`작성자`*` | `types:Asset` | 생성에 사용된 기본 자산의 자산 레코드입니다. |
| ` *`생성됨`*` | `types:Asset` | 생성된 자산의 자산 레코드입니다. |
| ` *`attributeArray`*` | `types:GenerationAttributeArray` | 생성 프로세스와 연관된 속성 배열입니다. |

