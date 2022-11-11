---
description: PostScript 파일 속성입니다.
solution: Experience Manager
title: GenerationInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9aac2973-bbcb-4914-9bf9-203f0357527c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '45'
ht-degree: 11%

---

# [!DNL GenerationInfo]{#generationinfo}

PostScript 파일 속성입니다.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| [!DNL engine] | `xsd:string` | 사용된 생성 엔진(값에 대한 &quot;생성 정보&quot; 참조). |
| [!DNL originator] | `types:Asset` | 생성에 사용된 기본 자산의 자산 레코드입니다. |
| [!DNL generated] | `types:Asset` | 생성된 자산의 자산 레코드입니다. |
| attributeArray | `types:GenerationAttributeArray` | 생성 프로세스와 연관된 속성 배열입니다. |
