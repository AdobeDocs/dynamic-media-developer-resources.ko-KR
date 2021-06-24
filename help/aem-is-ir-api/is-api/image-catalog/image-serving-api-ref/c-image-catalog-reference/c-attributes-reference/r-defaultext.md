---
description: 기본 이미지 파일 접미사입니다. 경로에 파일 접미사가 포함되지 않은 경우 카탈로그 경로(또는 카탈로그 MaskPath) 필드 값에 추가됩니다
solution: Experience Manager
title: DefaultExt
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 43b3e5b8-6374-458d-8503-8e04c8c84233
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 2%

---

# DefaultExt{#defaultext}

기본 이미지 파일 접미사입니다. 경로에 파일 접미사를 포함하지 않는 경우 다음 카탈로그에 추가됩니다.Path (또는 catalog::MaskPath) 필드 값에 추가됩니다.

파일 접미사는 마침표와 문자열 끝 사이의 하나 이상의 문자와 마침표로 구성됩니다. 경로가 카탈로그 항목으로 확인되지 않고 마지막 경로 요소에 파일 접미사가 포함되지 않은 경우 접미사는 http 경로에 추가됩니다.

## 속성 {#section-b024e6450b414ccc8b83a48a3b4e00f9}

텍스트 문자열입니다. 선행 &#39;.&#39;를 포함해야 합니다. 및 하나 이상의 문자.

## 기본값 {#section-1194c36ffe0748c5b9ff7d732a506588}

정의되지 않은 경우 `default::DefaultExt`에서 상속됩니다. 정의되었지만 비어 있는 경우 이 카탈로그를 사용할 때 이미지 이름에 기본 접미사가 적용되지 않습니다.

## 참조 {#section-d7c408b979844643adff8258f500eb7c}

[catalog::Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) ,  [catalog::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md)
