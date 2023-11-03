---
description: 이미지 제공은 간단한 시각적 워터마크 기능을 구현합니다.
solution: Experience Manager
title: 워터마크
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e744be3f-9753-4513-8f37-055fa03077cc
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---

# 워터마크{#watermarks}

이미지 제공은 간단한 시각적 워터마크 기능을 구현합니다.

워터마크는 일반적으로 반투명 이미지이지만 텍스트 또는 보다 복잡하고 계층화된 합성 이미지일 수 있습니다. 서버는 모든 보기 속성 다음에 응답 이미지 위에 워터마크를 계층화합니다( `wid=`, `hei=`, `align=`, `scl=`, `bgc=`)이 적용되었습니다.

워터마크는 설정에 의해 활성화됩니다. `attribute::Watermark` 워터마크 이미지 또는 템플릿을 포함하는 유효한 카탈로그 엔트리입니다. If `attribute::Watermark` 가 명명된 카탈로그에 설정되면 서버는 요청 URL에서 카탈로그 ID를 참조하는 모든 이미지 요청에 워터마크를 추가합니다. If `default::Watermark` 가 설정되어 있습니다(기본 카탈로그에서). [!DNL default.ini]) 워터마크는 카탈로그 참조 여부에 관계없이 모든 이미지 요청에 적용됩니다.

워터마크 는 썸네일 요청에 대해 반환된 이미지에 적용되지 않습니다( `req=tmb`) 및 Dynamic Media 뷰어의 특정 요청.

## 크기 조절 및 정렬 {#section-89ef9e5926ae438abbd8e70332749b76}

워터마크가 지정되면 서버는 먼저 합성 이미지( *대상 이미지*) 워터마크를 적용해야 하는 대상(뷰를 적용하기 전에 변환). 그런 다음 서버는 다른 이미지(와 마찬가지로 워터마크에 대한 합성 이미지를 생성합니다. *워터마크 이미지*).

표준 이미지와 달리 `sizeN=` 워터마크 이미지의 layer=0 또는 layer=comp에 대해 지정할 수 있습니다. 대상 이미지를 기준으로 워터마크 이미지의 크기를 조정할 수 있습니다. If `sizeN=` 가 지정되지 않은 경우 워터마크 이미지가 대상 이미지와 병합될 때 픽셀 크기가 유지됩니다.

요청 명령(예: `fmt=`) 및 보기 명령(예: `wid=`)는 워터마크 레코드에서 무시되며, `align=`. `align=` 워터마크 이미지를 타겟 이미지에 대해 상대적으로 배치하는데 사용될 수 있다. 이것은 타겟 이미지의 코너 또는 에지에 대한 워터마크의 위치를 허용한다.

크기 조절 및 정렬 후 서버는 다음을 사용하여 대상 이미지 위에 워터마크 이미지를 계층화합니다. `blendMode=` 및 `opac=` 다음에 대해 지정된 값 `layer=0` 또는 `layer=comp` 워터마크 이미지의 이름입니다. 마지막으로, 타겟 이미지에 대해 지정된 요청 및 뷰 명령이 적용되어 응답 이미지를 구성한다.

워터마크 이미지는에 의해 응답 이미지에 추가된 공백 위로 확장되지 않습니다. `wid=` 및 `hei=` 명령입니다.

## 예 {#section-0408c977d7324d4cb0e76a91cdfa2acd}

일반적인 워터마크는 로고 또는 저작권 표시가 포함된 간단한 RGBA 이미지로 구성될 수 있습니다. 다음을 사용하여 이미지 카탈로그(또는 기본 카탈로그)에 레코드를 만듭니다. `catalog::Id` 을 로 설정 `watermark` 및 워터마크 이미지 파일 지정 `catalog::Path`. 여백을 약간 남겨두고 워터마크를 보기 이미지에 맞게 늘리고(워터마크를 왜곡하지 않고) 불투명도를 원래 워터마크의 20%로 줄이려고 하므로 `catalog::Modifier` 끝 `sizeN=0.9,0.9&opac=20`. 워터마크를 활성화하려면 를 설정합니다. `attribute::Watermark` 워터마크 카탈로그 항목의 id에 대해, 이 예제에서는 &quot;watermark&quot;입니다. 우리는 다른 실험을 하고 싶을 수도 있다 `blendMode=` 다양한 워터마크 효과를 얻기 위한 선택 사항.

## 참조 {#section-4d66713abacb42c7b6a0c93cbf966a97}

[속성::워터마크](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b)
