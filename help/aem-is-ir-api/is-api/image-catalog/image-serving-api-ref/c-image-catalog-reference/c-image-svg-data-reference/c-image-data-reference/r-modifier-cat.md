---
description: 접두사 요청 수정자 문자열. '&' 문자로 구분된 이미지 제공 명령이 하나 이상 없습니다.
seo-description: 접두사 요청 수정자 문자열. '&' 문자로 구분된 이미지 제공 명령이 하나 이상 없습니다.
seo-title: 수정자
solution: Experience Manager
title: 수정자
topic: Scene7 Image Serving - Image Rendering API
uuid: eb17d115-22ec-4b1b-9039-9bd2bc256f48
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 7%

---


# 수정자{#modifier}

접두사 요청 수정자 문자열. &#39;&amp;&#39; 문자로 구분된 이미지 제공 명령이 하나 이상 없습니다.

이미지를 지속적으로 수정하고 템플릿 본문을 저장하는 데 사용됩니다.

이 필드의 명령은 이 레코드를 참조하는 요청이나 템플릿의 명령과 `catalog::PostModifier`의 명령에 의해 재정의됩니다

매크로는 동일한 카탈로그 또는 기본 카탈로그에 정의된 한 `catalog::Modifier`에서 허용됩니다. 사용자 지정 변수도 사용할 수 있습니다.

## 속성 {#section-6674388f77d644469371a17e8809c45f}

텍스트 문자열. 선택 사항입니다.

## 기본값 {#section-f4ffe8b75792435c8b1040e75c5fb8a1}

없음.

## 참조 {#section-7a67803d141b442180c418c1f3cff029}

[카탈로그::PostModifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-postmodifier-cat.md#reference-4bc3738a812b4e7c8a180e27bfbd770b)
