---
description: Postfix 요청 수정자 문자열입니다. '&'자로 구분된 이미지 제공 명령이 하나 이상 없습니다.
solution: Experience Manager
title: PostModifier
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7d6c9408-1f09-464d-8a69-eabdf7c0117d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 3%

---

# PostModifier{#postmodifier}

Postfix 요청 수정자 문자열입니다. &#39;&amp;&#39;자로 구분된 이미지 제공 명령이 하나 이상 없습니다.

이 필드의 명령은 항상 HTTP 요청과 `catalog::Modifier`의 명령을 재정의합니다.

`catalog::PostModifier`은(는) 특정 이미지에 `qlt=` 또는 `resmode=`과(와) 같이 일반적으로 URL에서 제어되는 특수 설정이 필요한 경우 유용합니다. `catalog::Modifier`은(는) 이미지 카탈로그에서 대부분의 IS 명령을 설정하는 데 사용해야 합니다.

매크로는 동일한 카탈로그나 기본 카탈로그에 정의되어 있는 한 `catalog::PostModifier`에서 사용할 수 있습니다. 사용자 지정 변수도 사용할 수 있습니다.

>[!NOTE]
>
>요청에 여러 레이어가 포함된 경우 레이어 0의 `catalog::PostModifier` 내용만 적용됩니다. 다른 모든 레이어 중 `catalog::PostModifier`개는 무시됩니다.

## 속성 {#section-6d5b0462ba1245b8ac3ddfd15c059f42}

텍스트 문자열입니다. 선택적.

## 기본값 {#section-8c83bce7f6c846d48fbe8fd30bedf5d5}

없음.

## 참조 {#section-8942f70e40f44dc48df51b4d8d0a7cde}

[catalog::Modifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834)
