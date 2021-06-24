---
description: PostScript 파일 속성입니다.
solution: Experience Manager
title: GenerationInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 9aac2973-bbcb-4914-9bf9-203f0357527c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 12%

---

# GenerationInfo{#generationinfo}

PostScript 파일 속성입니다.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| `*`엔진`*` | `xsd:string` | 사용된 생성 엔진(값에 대한 &quot;생성 정보&quot; 참조). |
| `*`작성자`*` | `types:Asset` | 생성에 사용된 기본 자산의 자산 레코드입니다. |
| `*`생성됨`*` | `types:Asset` | 생성된 자산의 자산 레코드입니다. |
| `*`attributeArray`*` | `types:GenerationAttributeArray` | 생성 프로세스와 연관된 속성 배열입니다. |
