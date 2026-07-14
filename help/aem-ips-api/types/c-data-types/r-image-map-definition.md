---
description: 브라우저에서 클릭 동작에 대한 대상 정의입니다.
solution: Experience Manager
title: 이미지 맵 정의
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 58478e7c-e3a1-4dd5-8ff9-e9752301b93c
TQID: 'https://experienceleague.adobe.com/x27LpaNACQ5k-n09O-9Bhw7aecAjWQ6wNkLt8XewVXs'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: b658a9f9067d2313c1c838c7e157f4070ebc2b50
workflow-type: tm+mt
source-wordcount: 71
ht-degree: 12%

---

# [!DNL ImageMapDefinition]{#imagemapdefinition}

브라우저에서 클릭 동작에 대한 대상 정의입니다.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| name | `xsd:string` | 이미지 맵 정의의 이름입니다. |
| shapeType | `xsd:string` | 영역 셰이프 값 중 하나. |
| 지역 | `xsd:string` | 이미지 맵 좌표. 형식은 HTML `<area>` 태그 특성을 기반으로 합니다. |
| 작업 | `xsd:string` | `href` URL을 포함하여 HTML `<area>` 태그에 포함할 기타 특성입니다. |
| 활성화됨 | `xsd:boolean` | 이미지 맵이 활성화된 경우 True입니다. |

