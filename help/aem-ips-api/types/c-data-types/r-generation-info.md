---
description: PostScript 파일 속성입니다.
solution: Experience Manager
title: GenerationInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9aac2973-bbcb-4914-9bf9-203f0357527c
TQID: 'https://experienceleague.adobe.com/fM-heKQFWRXUn8QWVxJA1yNJ2aqlozRoK5B-ErzamLA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 45
ht-degree: 11%

---

# [!DNL GenerationInfo]{#generationinfo}

PostScript 파일 속성입니다.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| [!DNL engine] | `xsd:string` | 사용된 생성 엔진(값은 &quot;생성 정보&quot; 참조). |
| [!DNL originator] | `types:Asset` | 생성에 사용되는 기본 에셋의 에셋 레코드. |
| [!DNL generated] | `types:Asset` | 생성된 에셋의 에셋 레코드. |
| attributeArray | `types:GenerationAttributeArray` | 생성 프로세스와 연결된 속성 배열입니다. |
