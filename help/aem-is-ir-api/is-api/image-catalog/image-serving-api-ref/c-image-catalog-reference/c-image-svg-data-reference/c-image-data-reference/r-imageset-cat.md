---
description: 이미지 집합 데이터. Scene7 뷰어에서 사용하는 정렬된 이미지 집합을 정의하고 속성을 제어하는 메커니즘을 제공합니다.
seo-description: 이미지 집합 데이터. Scene7 뷰어에서 사용하는 정렬된 이미지 집합을 정의하고 속성을 제어하는 메커니즘을 제공합니다.
seo-title: 이미지 집합
solution: Experience Manager
title: 이미지 집합
topic: Scene7 Image Serving - Image Rendering API
uuid: 1a34aaef-4053-4474-abb8-794331898d88
translation-type: tm+mt
source-git-commit: 06f227705765e4173e1c4b49dd7d8202884f5e07

---


# 이미지 집합{#imageset}

이미지 집합 데이터. Scene7 뷰어에서 사용하는 정렬된 이미지 집합을 정의하고 속성을 제어하는 메커니즘을 제공합니다.

이미지 세트는 하나 이상의 하위 항목(이미지 ID, 견본 ID, 미디어 파일 경로, 레이블 등)으로 구성된 정렬된 쉼표로 구분된 항목 목록으로 구성됩니다. 각 항목은 세미콜론 및/또는 콜론으로 구분됩니다.

중괄호 &#39;{ }&#39; 및 괄호 &#39;( )&#39;를 사용하여 특정 컨텐츠(예: 색상 값)를 구분하거나 중첩 집합을 나타낼 수 있습니다. 이 방법으로 사용된 중괄호 또는 괄호는 인코딩되지 않아야 하며 항상 일치하는 쌍으로 표시되어야 합니다. 그렇지 않으면 카탈로그 구문 분석 오류가 발생합니다.

>[!NOTE]
>
>다음 문자는 세트 구분 기호로 사용되며 ID 또는 문자열 값의 일부로 세트에 표시될 때 HTTP로 인코딩되어야 합니다.
>
>* ,
>* ;
>* :
>* {
>* }
>* (
>* )



이미지 세트의 구조 및 사용에 대한 자세한 내용은 이미지 제공 뷰어 설명서를 참조하십시오.

서버는 `req=imageset` 요청에 대한 응답으로 수정 없이 이 필드의 내용을 반환합니다.

## 표준 세트 {#section-5ecc8ffee7224668b63f601383665564}

다음 집합 정의는 이미지 제공에서 기본적으로 지원되며, 특정 뷰어와의 액세스에는 서버측 구문 분석, 유효성 검사 및 세트 처리가 포함됩니다. 각 세트 유형은 에서 해당 값을 지정하여 식별할 수 `catalog::AssetType`있습니다.

**기본 견본 집합**

기본 견본 세트의 각 항목은 이미지 레코드에 대한 참조와 견본으로 사용되는 이미지 레코드에 대한 선택적 개별 참조로 구성됩니다.

| ` *`basicSwatchSet`*` | ` *`견본`*&#42;[',' *`항목 견본 항목`*]` |
|---|---|
| ` *`swatchItem`*` | ` *``*[';' *`imageIdswatch`*]` |
| ` *`견본`*` | ` *`swatchId`*|solidColorSpecifier` |
| ` *`imageId`*` | IS 이미지 참조(카탈로그/ID) |
| ` *`swatchId`*` | IS 이미지 참조(카탈로그/ID) |
| ` *`solidColorSpecifier`*` | ` '{0x' *``* [ *`rggbblabel`*]'}'` |
| ` *`rggbb`*` | 단색 색상 견본을 위한 6자리 16진수 RGB 색상 값 |
| ` *`레이블`*` | 단색 색상 견본을 위한 선택적 텍스트 레이블 |

**계층 견본 집합**

계층 구조 견본 집합의 각 항목은 기본 견본 항목 또는 견본 집합 레코드에 대한 참조로 구성될 수 있습니다(이러한 항목에 대한 견본은 필수).

| ` *`hierarchicalSwatchSet`*` | ` *``* &#42;[ ',' *`계층적 견본 항목계층적 견본 항목`* ]` |
|---|---|
| ` *`hierarchicalSwatchItem`*` | ` *``* | { *``* ';' *`swatchItembasicSwatchSetIdswatch`* }` |
| ` *`basicSwatchSetId`*` | 기본 견본 집합을 정의하는 카탈로그 레코드에 대한 IS 참조(카탈로그/ID) |

**기본 스핀 세트**

기본 스핀 세트는 간단한 이미지 ID 목록으로 구성됩니다.

*`basicSpinSet imageId`*  *`[ ';'`  *`imageId`* `]`

**2차원 회전 집합**

2차원 회전 집합의 각 항목은 간단한 이미지, 기본 회전 집합에 대한 참조 또는 중괄호로 구분된 인라인 기본 회전 집합으로 구성될 수 있습니다. 중괄호 대신 괄호를 사용할 수 있습니다.

| ` *`2dSpinItem`*` | ` *`2dSpinSet`* *`2dSpinItem`* &#42;[ ',' *`2dSpinItem`* ]` |
|---|---|
| ` *`2dSpinItem`*` | ` *``* | { '{' *``* '}' } | *`imageIdbasicSpinSetbasicSpinSetId`*` |
| ` *`basicSpinSetId`*` | 기본 회전 집합을 정의하는 카탈로그 레코드에 대한 IS 참조(카탈로그/ID) |

**페이지 세트**

페이지 세트의 각 항목은 최대 3개의 페이지 이미지로 구성되며, 이 이미지는 콜론으로 구분됩니다.

| ` *`pageSet`*` | ` *`pageItem`* &#42;[ , *`항목`* ]` |
|---|---|
| ` *`pageItem`*` | ` *``* [ : *``* [ : *`imageIdimageIdimageId`* ] ]` |

**미디어 집합**

미디어 세트의 각 항목은 이미지, 기본 견본 세트, 계층적 견본 세트, 기본 스핀 세트, 2차원 스핀 세트, 페이지 세트 또는 비디오 자산으로 구성될 수 있습니다. 각 미디어 세트 항목에는 선택 사항 견본 및 유형 식별자가 포함될 수도 있습니다.

| ` *`mediaSet`*` | ` *``* &#42;[ , *`항목`* ]` |
|---|---|
| ` *`항목`*` | ` { *``* | *``* | *``*}} | *``* } [ ; [ *``* ] [ ; [ *`videoItemItemimageItemsetItemIDreserved`* ] ] ]` |
| ` *`videoItem`*` | ` *``* ; *`videoswatchId`*` |
| ` *`recutItem`*` | ` *``* ; *`recutswatchId`*` |
| ` *`imageItem`*` | ` *``* ; [ *`imageIdswatchId`* ]` |
| ` *`setItem`*` | ` { *``* | { '{' *``* '}' } } ; *`setIdinlineSetswatchId`*` |
| ` *`ID`*` | `media type identifier [ img | basic | advanced_image | img | img_set | advanced_imageset | advanced_swatchset | spin | video ]` |
| ` *`swatchId`*` | IS 이미지 ID |
| ` *`video`*` | 비디오/애니메이션 파일 경로 또는 정적 카탈로그 ID |
| ` *`rect`*` | 정의 XML 파일 경로 또는 정적 카탈로그 ID 다시 자르기 |
| ` *`imageId`*` | IS 이미지 ID |
| ` *`setId`*` | 이미지, 회전 또는 카탈로그 세트에 대한 참조임 |
| ` *`inlineSet`*` | 인라인 이미지, 회전 또는 카탈로그 집합 |
| ` *`reserved`*` | 향후 사용을 위해 예약됨 |

**Video Sets**

비디오 세트는 각 ID가 정적 컨텐츠 카탈로그의 항목을 참조하는 간단한 비디오 ID 목록으로 구성됩니다.

*`videoSet videoId`*  *`[ ,`  *`videoId`* `]`

## 속성 {#section-17c731e5c46646aa90ac21f39bb693ca}

텍스트 문자열. 쉼표로 구분된 `catalog::Id` 값 목록, 절대 이미지 서버 파일 경로 또는 관련 파일 경로 `attribute::RootPath`. 동일한 이미지가 세트에서 두 번 이상 참조할 수 있습니다. 정의된 카탈로그 레코드는 어느 위치에서나 세트에 표시될 수 있습니다.

이 필드는 텍스트 문자열 현지화에 참여하고 있습니다. 문자열(일부) *`label`* 외에 하나 이상의 &#39; *`solidColorSpecifier`*`^loc=…^`&#39; 로컬라이제이션 토큰이 포함된 모든 구분된 필드가 현지화되어 있습니다. 자세한 내용은 [HTTP 프로토콜](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) 참조 *문서의 텍스트 문자열 현지화를* 참조하십시오.

## 기본값 {#section-c3a60e360393478284f0f2d2da5b963b}

없음.

## 참조 {#section-4c99c44f99074aa0a4ed90ba183bbc25}

[req=imageset](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) , [attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md), [Object Id Translation,](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md) Text String Localization [](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) , Image Serving Viewers Documentation
