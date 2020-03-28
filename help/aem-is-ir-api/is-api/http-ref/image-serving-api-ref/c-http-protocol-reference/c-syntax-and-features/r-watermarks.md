---
description: 이미지 제공은 간단한 시각적 워터마크 기능을 구현합니다.
seo-description: 이미지 제공은 간단한 시각적 워터마크 기능을 구현합니다.
seo-title: 워터마크
solution: Experience Manager
title: 워터마크
topic: Scene7 Image Serving - Image Rendering API
uuid: b2bbaa59-dad9-4be3-bb92-142ed44f6d65
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 워터마크{#watermarks}

이미지 제공은 간단한 시각적 워터마크 기능을 구현합니다.

워터마크는 일반적으로 반투명 이미지이지만 텍스트 또는 보다 복잡하고 레이어로 구성된 합성 이미지일 수 있습니다. 모든 보기 속성(, `wid=`, `hei=`, `align=`, `scl=`, `bgc=`)이 적용된 후 서버에서 응답 이미지 위에 워터마크를레이어로 만듭니다.

워터마크는 워터마크 이미지 또는 템플릿이 들어 `attribute::Watermark` 있는 유효한 카탈로그 항목으로 설정하면 활성화됩니다. 명명된 카탈로그에 `attribute::Watermark` 설정된 경우 서버는 요청 URL에서 카탈로그 ID를 참조하는 모든 이미지 요청에 워터마크를 추가합니다. 기본 카탈로그의 경우 `default::Watermark` 워터마크가 카탈로그를 참조하는지 여부에 관계없이 모든 이미지 요청에 워터마크가 적용됩니다 [!DNL default.ini].

워터마크는 축소판 요청( `req=tmb`) 및 Scene7 뷰어의 특정 요청에 응답하여 반환된 이미지에 적용되지 않습니다.

## 크기 조절 및 정렬 {#section-89ef9e5926ae438abbd8e70332749b76}

워터마크를 지정하면 서버가 먼저 워터마크를 적용해야 하는 합성 이미지( *대상 이미지*)를 생성합니다(보기 변환을 적용하기 전에). 그런 다음 서버는 다른 이미지( *워터마크 이미지*)와 마찬가지로 워터마크의 합성 이미지를 생성합니다.

표준 이미지와 달리, 워터마크 이미지의 레이어=0 또는 layer=comp에 대해 지정할 `sizeN=` 수 있습니다. 따라서 대상 이미지를 기준으로 워터마크 이미지의 크기를 조정할 수 있습니다. 지정하지 `sizeN=` 않으면 대상 이미지와 병합될 때 워터마크 이미지의 픽셀 크기가 유지됩니다.

요청 명령( `fmt=`예: `wid=`) 및 보기 명령(예: `align=`)은 워터마크 레코드에서 무시되며, 예외적으로 무시됩니다. `align=` 대상 이미지를 기준으로 워터마크 이미지를 상대적으로 배치하기 위해 사용할 수 있습니다. 이렇게 하면 대상 이미지의 모서리 또는 가장자리를 기준으로 워터마크를 배치할 수 있습니다.

크기 조절 및 정렬 후 서버는 워터마크 이미지에 대해 `blendMode=` 또는 워터마크 이미지의 `opac=` 값과 함께 워터마크 이미지를 대상 이미지 위에 레이어로 `layer=0` `layer=comp` 지정합니다. 마지막으로 대상 이미지에 대해 지정된 요청 및 보기 명령이 응답 이미지를 구성하기 위해 적용됩니다.

워터마크 이미지는 `wid=` 및 `hei=` 명령으로 회신 이미지에 추가된 빈 공간을 넘어 확장되지 않습니다.

## 예 {#section-0408c977d7324d4cb0e76a91cdfa2acd}

일반적인 워터마크는 로고와 저작권 공지가 포함된 간단한 RGBA 이미지로 구성될 수 있습니다. 이미지 카탈로그(또는 기본 카탈로그)에 워터마크 이미지 파일을 `catalog::Id` 로 `watermark` 설정하고 로 지정하는 레코드를 만듭니다 `catalog::Path`. 워터마크를 축소하고 워터마크를 왜곡하지 않고 보기 이미지에 맞게 확대하려고 합니다. 이때 여백이 약간 남아 있으면 불투명도를 원본 워터마크의 20%로 줄여 `catalog::Modifier` 보겠습니다. 이렇게 `sizeN=0.9,0.9&opac=20`하면 워터마크를 활성화하려면 이 `attribute::Watermark` 예에서는 워터마크 카탈로그 항목의 ID인 &quot;워터마크&quot;로 설정합니다. 다양한 워터마크 효과를 내기 위해 다양한 `blendMode=` 옵션을 사용해 볼 수도 있습니다.

## 참조 {#section-4d66713abacb42c7b6a0c93cbf966a97}

[속성::워터마크](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b)
