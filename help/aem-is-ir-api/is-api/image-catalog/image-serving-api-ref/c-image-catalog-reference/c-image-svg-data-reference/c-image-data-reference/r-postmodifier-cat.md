---
description: Postfix 요청 수정자 문자열입니다. '&' 문자로 구분된 이미지 제공 명령이 하나 이상 없습니다.
solution: Experience Manager
title: PostModifier
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 7d6c9408-1f09-464d-8a69-eabdf7c0117d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 4%

---

# PostModifier{#postmodifier}

Postfix 요청 수정자 문자열입니다. &#39;&amp;&#39; 문자로 구분된 이미지 제공 명령이 하나 이상 없습니다.

이 필드의 명령은 항상 HTTP 요청과 `catalog::Modifier`의 명령을 재정의합니다.

`catalog::PostModifier` 특정 이미지에 일반적으로 또는 과 같은 URL에서 제어되는 특수 설정이 필요한 경우 `qlt=` 에 유용합니다 `resmode=`. `catalog::Modifier` 이미지 카탈로그에서 대부분의 IS 명령을 설정하는 데 사용해야 합니다.

매크로는 동일한 카탈로그나 기본 카탈로그에서 정의된 한 `catalog::PostModifier`에서 허용됩니다. 사용자 지정 변수도 사용할 수 있습니다.

>[!NOTE]
>
>요청에 여러 레이어가 포함된 경우 레이어 0의 `catalog::PostModifier` 컨텐츠만 적용됩니다. `catalog::PostModifier` 다른 모든 레이어는 무시됩니다.

## 속성 {#section-6d5b0462ba1245b8ac3ddfd15c059f42}

텍스트 문자열입니다. 선택 사항입니다.

## 기본값 {#section-8c83bce7f6c846d48fbe8fd30bedf5d5}

없음.

## 참조 {#section-8942f70e40f44dc48df51b4d8d0a7cde}

[카탈로그::수정자](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834)
