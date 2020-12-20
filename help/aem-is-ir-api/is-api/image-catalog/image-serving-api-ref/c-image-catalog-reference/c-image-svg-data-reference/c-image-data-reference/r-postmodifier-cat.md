---
description: 사후 수정 요청 수정자 문자열. '&' 문자로 구분된 이미지 제공 명령이 하나 이상 없습니다.
seo-description: 사후 수정 요청 수정자 문자열. '&' 문자로 구분된 이미지 제공 명령이 하나 이상 없습니다.
seo-title: PostModifier
solution: Experience Manager
title: PostModifier
topic: Scene7 Image Serving - Image Rendering API
uuid: 8800a9b2-e9c0-498b-b4e1-37952ba7c842
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 4%

---


# PostModifier{#postmodifier}

사후 수정 요청 수정자 문자열. &#39;&amp;&#39; 문자로 구분된 이미지 제공 명령이 하나 이상 없습니다.

이 필드의 명령은 항상 HTTP 요청과 `catalog::Modifier`의 명령을 재정의합니다.

`catalog::PostModifier` 은 특정 이미지에 URL에서 정상적으로 제어되는 특수 설정이 필요한 경우  `qlt=` 또는 `resmode=`와 같이 유용합니다. `catalog::Modifier` 이미지 카탈로그에서 대부분의 IS 명령을 설정하는 데 사용해야 합니다.

매크로는 동일한 카탈로그 또는 기본 카탈로그에 정의된 한 `catalog::PostModifier`에서 허용됩니다. 사용자 지정 변수도 사용할 수 있습니다.

>[!NOTE]
>
>요청에 여러 레이어가 포함된 경우 레이어 0의 `catalog::PostModifier` 내용만 적용됩니다. `catalog::PostModifier` 다른 모든 레이어는 무시됩니다.

## 속성 {#section-6d5b0462ba1245b8ac3ddfd15c059f42}

텍스트 문자열. 선택 사항입니다.

## 기본값 {#section-8c83bce7f6c846d48fbe8fd30bedf5d5}

없음.

## 참조 {#section-8942f70e40f44dc48df51b4d8d0a7cde}

[카탈로그::수정자](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834)
