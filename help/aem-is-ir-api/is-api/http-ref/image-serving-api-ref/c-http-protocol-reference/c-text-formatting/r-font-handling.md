---
title: 글꼴 처리
description: RTF 문자열에서 참조되는 모든 글꼴은 기본 카탈로그 또는 현재 이미지 카탈로그의 글꼴 맵 파일에서 사용할 수 있어야 합니다. 그렇지 않으면 오류가 반환됩니다.
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

RTF 문자열에서 참조되는 모든 글꼴은 기본 카탈로그 또는 현재 이미지 카탈로그의 글꼴 맵 파일에서 사용할 수 있어야 합니다. 그렇지 않으면 오류가 반환됩니다.

해당 글꼴 파일을 등록하면 기울임꼴 및 굵은 글꼴 텍스트에 가장 적합한 품질을 얻을 수 있습니다. 사용할 수 없는 경우 서버는 표준 면에서 굵은 글꼴 및/또는 기울임꼴 글꼴을 합성할 수 있습니다. (참조: [attribute::SynthesizeFontStyles](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md).

지정된 글꼴 `attribute::DefaultFont` RTF 문자열에 명시적으로 지정되지 않은 경우 가 사용됩니다.

이미지 제공은 TrueType, OpenType, Adobe Type 1(Windows만 해당) 글꼴을 지원합니다.

## Photofont® 글꼴 지원 {#section-74560ae898cf4708aba4c8b4093f5f00}

`textPs=` 는 다음과 같은 제한 사항을 가진 Photofont® 글꼴을 지원합니다.

* `\cf` 는 Photofont 글꼴을 지정하는 텍스트 범위에서 무시되며 Photofont 글꼴 면에는 미리 정의된 색상이 있습니다.
* 합성 글꼴 스타일은 지원되지 않습니다. `\b` 및 `\i`해당 글꼴 맵 항목이 필요합니다. 그렇지 않으면 오류가 반환됩니다

* 세로 텍스트 흐름은 지원되지 않습니다.
* 16비트 이미지가 있는 Photofont 글꼴은 지원되지 않습니다.
* 이미지당 여러 개의 글리프가 있는 Photofont 글꼴은 지원되지 않습니다
* Photofont 글리프 이미지에 색상 프로파일이 포함되어 있지 않은 경우 단조로운 색상 변환이 적용됩니다. 이 경우 상대 색도계 렌더링 의도 및 검은 점 보상이 항상 적용됩니다

을(를) 참조하십시오 [www.photofont.com](https://www.photofont.com) 추가 정보.

## 참조 {#section-6cb8a802aa044836bbe449d559093f3a}

[글꼴 맵 참조](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d), [attribute::SynthesizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15), [attribute::DefaultFont](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultfont.md#reference-48b763ac254545e89a25c76ff7581107), [ [!DNL www.photofont.com] ](https://www.photofont.com)
