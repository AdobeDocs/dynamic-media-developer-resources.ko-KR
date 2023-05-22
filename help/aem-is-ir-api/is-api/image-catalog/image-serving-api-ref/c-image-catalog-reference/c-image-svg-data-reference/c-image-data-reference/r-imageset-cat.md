---
description: 이미지 집합 데이터입니다. Dynamic Media 뷰어에서 사용하는 정렬된 이미지 세트와 제어 속성을 정의하는 메커니즘을 제공합니다.
solution: Experience Manager
title: 이미지 집합
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,User
exl-id: eacf0553-8cec-4a1d-80a5-6fe37b92b5bf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '684'
ht-degree: 2%

---

# 이미지 집합{#imageset}

이미지 집합 데이터입니다. Dynamic Media 뷰어에서 사용하는 정렬된 이미지 세트와 제어 속성을 정의하는 메커니즘을 제공합니다.

이미지 세트는 쉼표로 구분된 정렬된 항목 목록으로 구성되며, 각 항목은 하나 이상의 하위 항목(이미지 ID, 견본 ID, 미디어 파일 경로, 레이블 등)으로 구성되며 세미콜론 및/또는 콜론으로 구분됩니다.

중괄호 `{ }` 및 괄호 `( )` 특정 콘텐츠(예: 색상 값)를 구분하거나 중첩된 세트를 나타내는 데 사용할 수 있습니다. 이 방법으로 사용되는 중괄호나 괄호는 인코딩할 수 없으며 항상 일치하는 쌍으로 표시되어야 합니다. 그렇지 않으면 카탈로그 구문 분석 오류가 발생합니다.

>[!NOTE]
>
>다음 문자는 집합 구분 기호로 사용되며 ID 또는 문자열 값의 일부로 집합에 표시될 때 HTTP 인코딩이 적용되어야 합니다.
>
>* `,`
>* `;`
>* `:`
>* `{`
>* `}`
>* `(`
>* `)`



이미지 세트의 구조 및 사용에 대한 자세한 내용은 이미지 제공 뷰어 설명서 를 참조하십시오.

서버는 다음에 대한 응답으로 수정 없이 이 필드의 내용을 반환합니다. `req=imageset` 요청.

## 표준 세트 {#section-5ecc8ffee7224668b63f601383665564}

다음 집합 정의는 기본적으로 이미지 제공에서 지원되며, 특정 뷰어에 대한 액세스는 서버 측 구문 분석, 유효성 검사 및 집합 처리와 관련되어 있습니다. 각 세트 유형은에서 해당 값을 지정하여 식별할 수 있습니다. `catalog::AssetType`.

**기본 견본 집합**

기본 견본 세트의 각 항목은 이미지 레코드에 대한 참조와 견본으로 사용되는 이미지 레코드에 대한 선택적 개별 참조로 구성됩니다.

| `*`기본 견본 집합`*` | `*`견본 항목`*&#42;[',' *`견본 항목`*]` |
|---|---|
| `*`견본 항목`*` | `*`imageId`*[';' *`견본`*]` |
| `*`견본`*` | `*`견본 ID`*|solidColorSpecifier` |
| `*`imageId`*` | IS 이미지 참조 (catalog/id) |
| `*`견본 ID`*` | IS 이미지 참조 (catalog/id) |
| `*`solidColorSpecifier`*` | ` '{0x' *`rrggbb`* [ *`레이블`*]'}'` |
| `*`rrggbb`*` | 단색 색상 견본을 위한 6자리 16진수 RGB 색상 값 포장 |
| `*`레이블`*` | 단색 색상 견본의 선택적 텍스트 레이블 |

**계층 구조 견본 집합**

계층적 견본 세트의 각 항목은 기본 견본 항목 또는 견본 세트 레코드에 대한 참조로 구성될 수 있습니다(이러한 항목에는 견본이 필요합니다).

| `*`계층 구조 견본 집합`*` | `*`계층 구조 견본 항목`* &#42;[ ',' *`계층 구조 견본 항목`* ]` |
|---|---|
| `*`계층 구조 견본 항목`*` | `*`견본 항목`* | { *`basicSwatchSetId`* ';' *`견본`* }` |
| `*`basicSwatchSetId`*` | 기본 견본 집합을 정의하는 카탈로그 레코드에 대한 IS 참조(카탈로그/ID) |

**기본 스핀 세트**

기본 회전 세트는 이미지 ID의 간단한 목록으로 구성됩니다.

*`basicSpinSet imageId`*  &#42;`[ ';'`  *`imageId`* `]`

**2차원 스핀 세트**

2차원 회전 집합의 각 항목은 간단한 이미지, 기본 회전 집합에 대한 참조 또는 중괄호로 구분된 인라인 기본 회전 집합으로 구성될 수 있습니다. 중괄호 대신 괄호를 사용할 수 있습니다.

| `*`2dSpinItem`*` | `*`2d회전 집합`* *`2d스핀 항목`* &#42;[ ',' *`2d스핀 항목`* ]` |
|---|---|
| `*`2dSpinItem`*` | `*`imageId`* | { '{' *`기본 회전 집합`* '}' } | *`basicSpinSetId`*` |
| `*`basicSpinSetId`*` | 기본 회전 집합을 정의하는 카탈로그 레코드에 대한 IS 참조(catalog/id) |

**페이지 세트**

페이지 세트의 각 항목은 콜론으로 구분된 최대 3개의 페이지 이미지로 구성될 수 있습니다.

| `*`pageSet`*` | `*`pageItem`* &#42;[ , *`pageItem`* ]` |
|---|---|
| `*`pageItem`*` | `*`imageId`* [ : *`imageId`* [ : *`imageId`* ] ]` |

**미디어 집합**

미디어 세트의 각 항목은 이미지, 기본 견본 세트, 계층 견본 세트, 기본 회전 세트, 2차원 회전 세트, 페이지 세트 또는 비디오 에셋으로 구성될 수 있습니다. 각 미디어 세트 항목에는 선택적 견본과 유형 식별자가 포함될 수도 있습니다.

| `*`mediaSet`*` | `*`항목`* &#42;[ , *`항목`* ]` |
|---|---|
| `*`항목`*` | ` { *`videoItem`* | *`recutItem`* | *`imageItem`*}} | *`setItem`* } [ ; [ *`ID`* ] [ ; [ *`예약됨`* ] ] ]` |
| `*`videoItem`*` | `*`비디오`* ; *`견본 ID`*` |
| `*`recutItem`*` | `*`다시 자르기`* ; *`견본 ID`*` |
| `*`imageItem`*` | `*`imageId`* ; [ *`견본 ID`* ]` |
| `*`setItem`*` | ` { *`setId`* | { '{' *`inlineSet`* '}' } } ; *`견본 ID`*` |
| `*`ID`*` | `media type identifier [ img | basic | advanced_image | img | img_set | advanced_imageset | advanced_swatchset | spin | video ]` |
| `*`견본 ID`*` | IS 이미지 ID |
| `*`비디오`*` | 비디오/애니메이션 파일 경로 또는 정적 카탈로그 ID |
| `*`다시 자르기`*` | 다시 자르기 정의 XML 파일 경로 또는 정적 카탈로그 ID |
| `*`imageId`*` | IS 이미지 ID |
| `*`setId`*` | 이미지, 스핀 또는 전자 카탈로그 세트에 대한 IS 참조 |
| `*`inlineSet`*` | 인라인 이미지, 회전 또는 전자 카탈로그 집합 |
| `*`reserved`*` | 향후 사용을 위해 예약됨 |

**Video Sets**

비디오 세트는 각 ID가 정적 콘텐츠 카탈로그의 항목을 참조하는 간단한 비디오 ID 목록으로 구성됩니다.

*`videoSet videoId`*  &#42;`[ ,`  *`videoId`* `]`

## 속성 {#section-17c731e5c46646aa90ac21f39bb693ca}

텍스트 문자열입니다. 쉼표로 구분된 목록 `catalog::Id` 값, 절대 이미지 서버 파일 경로 또는 상대 파일 경로 `attribute::RootPath`. 세트에서 동일한 이미지를 두 번 이상 참조할 수 있습니다. 정의된 카탈로그 레코드는 임의의 위치에 있는 세트에 나타날 수 있습니다.

이 필드는 텍스트 문자열 현지화에 적용됩니다. 에 더하여 *`label`* 문자열(일부) *`solidColorSpecifier`*) 하나 이상의 &#39;&#39;가 포함된 경우 구분된 모든 필드가 현지화됩니다. `^loc=…^`&#39; 현지화 토큰. 을(를) 참조하십시오 [텍스트 문자열 로컬라이제이션](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) 다음에서 *HTTP 프로토콜 참조* 을 참조하십시오.

## 기본값 {#section-c3a60e360393478284f0f2d2da5b963b}

없음.

## 참조 {#section-4c99c44f99074aa0a4ed90ba183bbc25}

[req=imageset](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) , [attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md), [개체 ID 변환](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md) , [텍스트 문자열 로컬라이제이션](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) , 이미지 제공 뷰어 설명서
