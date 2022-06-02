---
title: 글꼴 처리
description: RTF 문자열에서 참조되는 모든 글꼴은 기본 카탈로그의 글꼴 맵 파일 또는 현재 이미지 카탈로그에서 사용할 수 있어야 합니다. 그렇지 않으면 오류가 반환됩니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f24edd53-4b21-4147-9b50-95e616279aa8
source-git-commit: e1f0f8bdac2b7a8397adac3bb9ba38d0c519f8fb
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 0%

---

# 글꼴 처리{#font-handling}

RTF 문자열에서 참조되는 모든 글꼴은 기본 카탈로그의 글꼴 맵 파일 또는 현재 이미지 카탈로그에서 사용할 수 있어야 합니다. 그렇지 않으면 오류가 반환됩니다.

기울임체 및 굵은 글꼴 텍스트에 가장 좋은 품질은 해당 글꼴 파일을 등록함으로써 달성됩니다. 사용할 수 없는 경우 서버는 표준 얼굴에서 굵게 및/또는 기울임체 글꼴 얼굴을 합성할 수 있습니다. (자세한 내용은 [attribute::SynthizeFontStyles](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md).

지정한 글꼴면 `attribute::DefaultFont` RTF 문자열에서 명시적으로 지정하지 않은 경우 이 사용됩니다.

이미지 제공 기능은 TrueType, OpenType, Adobe Type 1(Windows 전용) 글꼴을 지원합니다.

## Photoshop® 글꼴 지원 {#section-74560ae898cf4708aba4c8b4093f5f00}

`textPs=` 에서는 다음과 같은 제한 사항이 있는 Photoshop® 글꼴을 지원합니다.

* `\cf` 는 Photoshop 글꼴 글꼴을 지정하는 텍스트 범위에서 무시됩니다. 광글꼴 글꼴에는 사전 정의된 색상이 있습니다
* 합성 글꼴 스타일은 지원되지 않습니다. 사용 `\b` 및 `\i`해당 글꼴 맵 항목이 필요합니다. 그렇지 않으면 오류가 반환됩니다

* 세로 텍스트 흐름은 지원되지 않습니다
* 16비트 이미지가 포함된 Photoshop 글꼴은 지원되지 않습니다
* 이미지당 여러 글리프가 있는 Photoshop 글꼴 글꼴은 지원되지 않습니다
* Photoshop Font Glyph 이미지 포함 색상 프로파일이 없으면 색상 변환 기능이 적용되지 않습니다. 이 경우 상대적 색상 지표 렌더링 의도 및 블랙포인트 보상이 항상 적용됩니다

을(를) 참조하십시오. [www.photofont.com](https://www.photofont.com) 추가 정보.

## 참조 {#section-6cb8a802aa044836bbe449d559093f3a}

[글꼴 맵 참조](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d), [attribute::SynthizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15), [attribute::DefaultFont](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultfont.md#reference-48b763ac254545e89a25c76ff7581107), [ [!DNL www.photofont.com] ](https://www.photofont.com)
