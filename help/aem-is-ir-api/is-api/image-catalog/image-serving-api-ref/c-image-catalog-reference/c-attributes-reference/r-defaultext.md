---
description: 기본 이미지 파일 접미사. 경로에 파일 접미사를 포함하지 않는 경우 카탈로그 경로(또는 카탈로그 MaskPath) 필드 값에 추가됩니다.
seo-description: 기본 이미지 파일 접미사. 경로에 파일 접미사를 포함하지 않는 경우 카탈로그 경로(또는 카탈로그 MaskPath) 필드 값에 추가됩니다.
seo-title: DefaultExt
solution: Experience Manager
title: DefaultExt
topic: Dynamic Media Image Serving - Image Rendering API
uuid: aa245d18-15cc-41cb-a49d-757d74fe6231
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 2%

---


# DefaultExt{#defaultext}

기본 이미지 파일 접미사. 경로에 파일 접미어를 포함하지 않는 경우 카탈로그에 추가된::Path(또는 catalog::MaskPath) 필드 값

파일 접미사는 마침표와 문자열 끝 사이에 마침표와 하나 이상의 문자로 구성됩니다. 경로가 카탈로그 항목으로 확인되지 않고 마지막 경로 요소에 파일 접미어를 포함하지 않는 경우 http 경로에 접미어가 추가됩니다.

## 속성 {#section-b024e6450b414ccc8b83a48a3b4e00f9}

텍스트 문자열. 행간 &#39;.&#39;을(를) 포함해야 합니다. 및 하나 이상의 문자를 사용할 수 있습니다.

## 기본값 {#section-1194c36ffe0748c5b9ff7d732a506588}

정의되지 않은 경우 `default::DefaultExt`에서 상속됩니다. 이 카탈로그를 사용할 때 기본 접미사가 이미지 이름에 적용되지 않는 것으로 정의되어 있지만 비어 있으면 이 카탈로그를 사용할 수 있습니다.

## 참조 {#section-d7c408b979844643adff8258f500eb7c}

[카탈로그::Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) ,  [카탈로그::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md)
