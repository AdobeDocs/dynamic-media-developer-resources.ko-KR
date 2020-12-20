---
description: 이미지 집합 데이터. Scene7 뷰어에서 사용하는 이미지 정렬 세트와 컨트롤 속성을 정의하는 메커니즘을 제공합니다.
seo-description: 이미지 집합 데이터. Scene7 뷰어에서 사용하는 이미지 정렬 세트와 컨트롤 속성을 정의하는 메커니즘을 제공합니다.
seo-title: 이미지 집합
solution: Experience Manager
title: 이미지 집합
topic: Scene7 Image Serving - Image Rendering API
uuid: 1a34aaef-4053-4474-abb8-794331898d88
translation-type: tm+mt
source-git-commit: 515fcf8488eba7d9ca501a4182eaa73f1936488b
workflow-type: tm+mt
source-wordcount: '703'
ht-degree: 2%

---


# 이미지 집합{#imageset}

이미지 집합 데이터. Scene7 뷰어에서 사용하는 이미지 정렬 세트와 컨트롤 속성을 정의하는 메커니즘을 제공합니다.

이미지 세트는 하나 이상의 하위 항목(이미지 ID, 견본 ID, 미디어 파일 경로, 레이블 등)을 세미콜론 및/또는 콜론으로 구분하여 정렬된 쉼표로 구분된 항목 목록으로 구성됩니다.

중괄호 `{ }` 및 괄호 `( )`는 특정 컨텐츠(예: 색상 값)를 구분하거나 중첩된 집합을 나타내는 데 사용할 수 있습니다. 이 방법으로 사용된 중괄호 또는 괄호는 인코딩할 수 없으며 항상 일치하는 쌍으로 표시되어야 합니다. 그렇지 않으면 카탈로그 구문 분석 오류가 발생합니다.

>[!NOTE]
>
>다음 문자는 세트 구분 기호로 사용되며 ID 또는 문자열 값의 일부로 세트에 표시될 때 HTTP로 인코딩되어야 합니다.
>
>* `,`
>* `;`
>* `:`
>* `{`
>* `}`
>* `(`
>* `)`



이미지 세트의 구조 및 사용에 대한 자세한 내용은 이미지 제공 뷰어 설명서를 참조하십시오.

서버는 `req=imageset` 요청에 대해 수정 없이 이 필드의 내용을 반환합니다.

## 표준 세트 {#section-5ecc8ffee7224668b63f601383665564}

다음 세트 정의는 이미지 제공 기능에서 기본적으로 지원되며, 특정 뷰어와의 액세스에는 서버측 구문 분석, 유효성 검사 및 세트 처리가 포함됩니다. 각 세트 유형은 `catalog::AssetType`에 해당 값을 지정하여 식별할 수 있습니다.

**기본 견본 집합**

기본 견본 세트의 각 항목은 이미지 레코드에 대한 참조와 견본으로 사용되는 이미지 레코드에 대한 별도의 참조(선택 사항)로 구성됩니다.

| ` *`basicSwatchSet`*` | ` *``*&#42;[',' *`swatchItemswatchItem`*]` |
|---|---|
| ` *`swatchItem`*` | ` *``*[';' *`imageIdswatch`*]` |
| ` *`견본`*` | ` *`swatchId`*|solidColorSpecifier` |
| ` *`imageId`*` | IS 이미지 참조(카탈로그/ID) |
| ` *`swatchId`*` | IS 이미지 참조(카탈로그/ID) |
| ` *`solidColorSpecifier`*` | ` '{0x' *``* [ *`rggbblabel`*]'}'` |
| ` *`rggbb`*` | 단색 색상 견본을 위한 6자리 16진수 RGB 색상 값 압축 |
| ` *`레이블`*` | 단색 색상 견본을 위한 텍스트 레이블(선택 사항) |

**계층적 견본 집합**

계층 구조 견본 세트의 각 항목은 기본 견본 항목 또는 견본 집합 레코드에 대한 참조로 구성될 수 있습니다(이러한 항목에 대한 견본은 필수).

| ` *`hierarchicalSwatchSet`*` | ` *``* &#42;[ ',' *`hierarchicalSwatchItemetricSwatchItem`* ]` |
|---|---|
| ` *`hierarchicalSwatchItem`*` | ` *``* | { *``* ';' *`swatchItembasicSwatchSetIdswatch`* }` |
| ` *`basicSwatchSetId`*` | 기본 견본 집합을 정의하는 카탈로그 레코드에 대한 IS 참조(카탈로그/ID) |

**기본 스핀 세트**

기본 회전 집합은 간단한 이미지 ID 목록으로 구성됩니다.

*`basicSpinSet imageId`*  *`[ ';'`  *`imageId`* `]`

**2차원 회전 집합**

2차원 회전 집합의 각 항목은 간단한 이미지, 기본 회전 집합 참조 또는 중괄호로 구분된 인라인 기본 회전 집합으로 구성될 수 있습니다. 중괄호 대신 괄호를 사용할 수 있습니다.

| ` *`2dSpinItem`*` | ` *`2dSpinSet`* *`2dSpinItem`* &#42;[ ',' *`2dSpinItem`* ]` |
|---|---|
| ` *`2dSpinItem`*` | ` *``* | { '{' *``* '}' } | *`imageIdbasicSpinSetbasicSpinSetId`*` |
| ` *`basicSpinSetId`*` | 기본 회전 집합을 정의하는 카탈로그 레코드에 대한 IS 참조(카탈로그/ID) |

**페이지 세트**

페이지 세트의 각 항목은 콜론으로 구분된 최대 3개의 페이지 이미지로 구성될 수 있습니다.

| ` *`pageSet`*` | ` *``* &#42;[ , *`pageItemItem`* ]` |
|---|---|
| ` *`pageItem`*` | ` *``* [ : *``* [ : *`imageIdimageIdimageId`* ] ]` |

**미디어 집합**

미디어 세트의 각 항목은 이미지, 기본 견본 세트, 계층적 견본 세트, 기본 스핀 세트, 2차원 스핀 세트, 페이지 세트 또는 비디오 에셋으로 구성될 수 있습니다. 각 미디어 세트 항목에는 선택 사항 견본 및 유형 식별자가 포함될 수도 있습니다.

| ` *`mediaSet`*` | ` *``* &#42;[ , *`항목`* ]` |
|---|---|
| ` *`항목`*` | ` { *``* | *``* | *``*}} | *``* } [ ; [ *``* ] [ ; [ *`videoItemrecutItemimageItemsetItemIDreserved`* ] ] ]` |
| ` *`videoItem`*` | ` *``* ; *`videoswatchId`*` |
| ` *`recutItem`*` | ` *``* ; *`recutswatchId`*` |
| ` *`imageItem`*` | ` *``* ; [ *`imageIdswatchId`* ]` |
| ` *`setItem`*` | ` { *``* | { '{' *``* '}' } } ; *`setIdinlineSetswatchId`*` |
| ` *`ID`*` | `media type identifier [ img | basic | advanced_image | img | img_set | advanced_imageset | advanced_swatchset | spin | video ]` |
| ` *`swatchId`*` | IS 이미지 ID |
| ` *`비디오`*` | 비디오/애니메이션 파일 경로 또는 정적 카탈로그 ID |
| ` *`recut`*` | 정의 XML 파일 경로 또는 정적 카탈로그 ID 다시 자르기 |
| ` *`imageId`*` | IS 이미지 ID |
| ` *`setId`*` | 이미지, 회전 또는 카탈로그 집합에 대한 참조임 |
| ` *`inlineSet`*` | 이미지, 회전 또는 카탈로그 세트 |
| ` *`reserved`*` | 향후 사용을 위해 예약됨 |

**Video Sets**

비디오 세트는 각 id가 정적 컨텐츠 카탈로그의 항목을 참조하는 간단한 비디오 ID 목록으로 구성됩니다.

*`videoSet videoId`*  *`[ ,`  *`videoId`* `]`

## 속성 {#section-17c731e5c46646aa90ac21f39bb693ca}

텍스트 문자열. `catalog::Id` 값의 쉼표로 구분된 목록, 절대 이미지 서버 파일 경로 또는 `attribute::RootPath`에 상대적인 파일 경로. 동일한 이미지가 세트에서 두 번 이상 참조할 수 있습니다. 정의된 카탈로그 레코드는 모든 위치의 세트에 표시될 수 있습니다.

이 필드는 텍스트 문자열 현지화에 참여합니다. *`label`* 문자열(*`solidColorSpecifier`*&#x200B;의 일부) 외에 하나 이상의 &#39; `^loc=…^`&#39; 현지화 토큰이 포함된 모든 구분된 필드가 현지화되어 있습니다. 자세한 내용은 *HTTP 프로토콜 참조*&#x200B;의 [텍스트 문자열 현지화](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)를 참조하십시오.

## 기본값 {#section-c3a60e360393478284f0f2d2da5b963b}

없음.

## 참조 {#section-4c99c44f99074aa0a4ed90ba183bbc25}

[req=imageset](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) ,  [속성::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md),  [개체 ID 번역](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md) ,  [텍스트 문자열 로컬라이제이션](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) , 이미지 제공 뷰어 설명서
