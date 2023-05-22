---
description: 접두사 요청 수정자 문자열. '&'자로 구분된 이미지 제공 명령이 하나 이상 없습니다.
solution: Experience Manager
title: 수정자
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6eef3159-c082-469b-b9dc-29acb28560d6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 7%

---

# 수정자{#modifier}

접두사 요청 수정자 문자열. &#39;&amp;&#39;자로 구분된 이미지 제공 명령이 하나 이상 없습니다.

이미지를 지속적으로 수정하고 템플릿 본문을 저장하는 데 사용됩니다.

이 필드의 명령은 이 레코드가 참조되는 요청 또는 템플릿의 동일한 명령과 의 명령에 의해 재정의됩니다 `catalog::PostModifier`

매크로는에서 허용됩니다. `catalog::Modifier`동일한 카탈로그나 기본 카탈로그에 정의되어 있는 한 사용할 수 있습니다. 사용자 지정 변수도 사용할 수 있습니다.

## 속성 {#section-6674388f77d644469371a17e8809c45f}

텍스트 문자열입니다. 선택적.

## 기본값 {#section-f4ffe8b75792435c8b1040e75c5fb8a1}

없음.

## 참조 {#section-7a67803d141b442180c418c1f3cff029}

[catalog::PostModifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-postmodifier-cat.md#reference-4bc3738a812b4e7c8a180e27bfbd770b)
