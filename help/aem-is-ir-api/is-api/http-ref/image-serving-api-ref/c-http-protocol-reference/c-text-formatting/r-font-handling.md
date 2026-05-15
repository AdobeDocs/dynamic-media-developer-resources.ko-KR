---
title: 글꼴 처리
description: RTF 문자열에서 참조되는 모든 글꼴은 기본 카탈로그 또는 현재 이미지 카탈로그의 글꼴 맵 파일에서 사용할 수 있어야 합니다. 그렇지 않으면 오류가 반환됩니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f24edd53-4b21-4147-9b50-95e616279aa8
TQID: 'https://experienceleague.adobe.com/KMD5vdWHM8HYsCO6UtJpPpTBfg9VJufhvsFsfOJiHv8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 134
ht-degree: 1%

---

# 글꼴 처리{#font-handling}

RTF 문자열에서 참조되는 모든 글꼴은 기본 카탈로그 또는 현재 이미지 카탈로그의 글꼴 맵 파일에서 사용할 수 있어야 합니다. 그렇지 않으면 오류가 반환됩니다.

해당 글꼴 파일을 등록하면 기울임꼴 및 굵은 글꼴 텍스트에 가장 적합한 품질을 얻을 수 있습니다. 사용할 수 없는 경우 서버는 표준 면에서 굵은 글꼴 및/또는 기울임꼴 글꼴을 합성할 수 있습니다. [attribute::SynthesizeFontStyles](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md)을(를) 참조하십시오.

RTF 문자열에 명시적으로 지정되지 않은 경우 `attribute::DefaultFont`(으)로 지정된 글꼴 이름이 사용됩니다.

이미지 제공에서는 TrueType, ®, Adobe Type 1(Windows에만 해당) 글꼴을 지원합니다.

<!--
 THIS APPEARS TO BE VERY OLD OUTDATED INFORMATION; URL IS DEAD TOO ## Photofont&reg; font support {#section-74560ae898cf4708aba4c8b4093f5f00}

Photofont&reg; fonts support `textPs=`, with the following restrictions:

* `\cf` is ignored in text spans that specify a Photofont font; Photofont font faces have predefined colors 
* Synthesized font styles are not supported; use of `\b` and `\i`require corresponding font map entries, otherwise an error is returned 

* Vertical text flow is not supported 
* Photofont fonts with 16-bit images are not supported 
* Photofont fonts with multiple glyphs per image are not supported 
* Naïve color conversion is applied unless the Photofont glyph images embed color profiles; in this case, relative colorimetric render intent and blackpoint compensation are always applied

See [https://www.photofont.com](https://www.photofont.com) for additional information.
-->

## 참조 {#section-6cb8a802aa044836bbe449d559093f3a}

[글꼴 맵 참조](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d), [특성::SynthesizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15), [특성::DefaultFont](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultfont.md#reference-48b763ac254545e89a25c76ff7581107)
