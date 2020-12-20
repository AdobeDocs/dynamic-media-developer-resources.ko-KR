---
description: RTF 문자열에서 참조하는 모든 글꼴은 기본 카탈로그나 현재 이미지 카탈로그의 글꼴 맵 파일에서 사용할 수 있어야 합니다. 그렇지 않으면 오류가 반환됩니다.
seo-description: RTF 문자열에서 참조하는 모든 글꼴은 기본 카탈로그나 현재 이미지 카탈로그의 글꼴 맵 파일에서 사용할 수 있어야 합니다. 그렇지 않으면 오류가 반환됩니다.
seo-title: 글꼴 처리
solution: Experience Manager
title: 글꼴 처리
topic: Scene7 Image Serving - Image Rendering API
uuid: 6a751973-5dae-472e-a908-bf24fa59d031
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 1%

---


# 글꼴 처리{#font-handling}

RTF 문자열에서 참조하는 모든 글꼴은 기본 카탈로그나 현재 이미지 카탈로그의 글꼴 맵 파일에서 사용할 수 있어야 합니다. 그렇지 않으면 오류가 반환됩니다.

해당 글꼴 파일을 등록하면 기울임체 및 굵은 글꼴 텍스트의 최고 품질을 얻을 수 있습니다. 사용할 수 없는 경우 서버는 표준 표면에서 굵게 및/또는 기울임체 글꼴 얼굴을 합성할 수 있습니다. (자세한 내용은 ` [attribute::SynthesizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15)`을 참조하십시오.)

`attribute::DefaultFont`으로 지정된 글꼴 인터페이스는 RTF 문자열에 명시적으로 지정된 글꼴이 없을 때 사용됩니다.

이미지 제공은 TrueType, OpenType, Adobe Type 1(Windows 전용) 글꼴을 지원합니다.

## Photoshop® 글꼴 지원 {#section-74560ae898cf4708aba4c8b4093f5f00}

`textPs=` 에서는 Photoshop® 글꼴을 지원하지만 다음 제한 사항이 있습니다.

* `\cf` 는 Photoshop 글꼴 글꼴을 지정하는 텍스트 범위에서 무시됩니다.Photofont 글꼴 얼굴에 사전 정의된 색상이 있습니다.
* 합성된 글꼴 스타일은 지원되지 않습니다.`\b` 및 `\i`을 사용하려면 해당 글꼴 맵 항목이 필요하며 그렇지 않으면 오류가 반환됩니다.

* 세로 텍스트 흐름은 지원되지 않습니다.
* 16비트 이미지가 포함된 Photoshop 글꼴 기능은 지원되지 않습니다.
* 이미지당 여러 글리프가 있는 Photoshop 글꼴 글꼴은 지원되지 않습니다.
* Photoshop 글리프 이미지에 색상 프로파일이 포함되지 않는 한 기본 색상 변환이 적용됩니다.이 경우 상대적인 색도계 렌더링 의도와 검은 점 보정이 항상 적용됩니다

자세한 내용은 ` [www.photofont.com](http://www.photofont.com)`을 참조하십시오.

## 참조 {#section-6cb8a802aa044836bbe449d559093f3a}

[글꼴 맵 참조](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d),  [속성::SyncizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15),  [속성::DefaultFont](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultfont.md#reference-48b763ac254545e89a25c76ff7581107),  [ [!DNL www.photofont.com] ](http://www.photofont.com)
