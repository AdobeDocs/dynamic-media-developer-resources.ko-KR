---
description: 이미지 제공 서비스는 간단한 시각적 워터마크 기능을 구현합니다.
solution: Experience Manager
title: 워터마크
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e744be3f-9753-4513-8f37-055fa03077cc
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 1%

---

# 워터마크{#watermarks}

이미지 제공 서비스는 간단한 시각적 워터마크 기능을 구현합니다.

워터마크는 일반적으로 반투명 이미지만 텍스트일 수도 있고 더 복잡한 레이어 복합 이미지입니다. 서버는 모든 보기 특성( `wid=`, `hei=`, `align=`, `scl=`, `bgc=`)이 적용되었습니다.

워터마킹은 `attribute::Watermark` 워터마크 이미지 또는 템플릿이 들어 있는 유효한 카탈로그 항목으로 이동합니다. If `attribute::Watermark` 가 명명된 카탈로그에서 설정된 경우, 서버는 요청 URL에서 카탈로그 id를 참조하는 모든 이미지 요청에 워터마크를 추가합니다. If `default::Watermark` 이(가) 설정되어 있습니다. 기본 카탈로그에서 [!DNL default.ini]). 워터마크는 카탈로그를 참조하는지 여부에 관계없이 모든 이미지 요청에 적용됩니다.

워터마크는 축소판 요청에 응답하여 반환된 이미지에 적용되지 않습니다( `req=tmb`)과 Dynamic Media 뷰어의 특정 요청 등에 사용할 수 있습니다.

## 크기 조절 및 정렬 {#section-89ef9e5926ae438abbd8e70332749b76}

워터마크를 지정하면 서버가 먼저 복합 이미지( *타겟 이미지*) 워터마크를 적용해야 하는 대상(보기 변형을 적용하기 전)입니다. 그러면 서버는 다른 이미지와 마찬가지로 워터마크의 합성 이미지를 생성합니다. *워터마크 이미지*).

표준 이미지와 달리 `sizeN=` layer=0 또는 layer=comp에 대해 지정할 수 있습니다. 이를 통해 대상 이미지를 기준으로 워터마크 이미지의 크기를 조정할 수 있습니다. If `sizeN=` 를 지정하지 않으면 대상 이미지와 병합될 때 워터마크 이미지의 픽셀 크기가 유지됩니다.

요청 명령(예: `fmt=`) 및 view 명령(예: `wid=`)은 워터마크 레코드에서 무시되며 `align=`. `align=` 대상 이미지를 기준으로 하여 워터마크 이미지를 배치하기 위해 사용할 수 있습니다. 이를 통해 대상 이미지의 모서리나 모서리에 대해 워터마크 위치를 지정할 수 있습니다.

크기 조절 및 정렬 후에 서버는 을 사용하여 대상 이미지 위에 워터마크 이미지를 레이어에 지정합니다 `blendMode=` 및 `opac=` 에 지정된 값 `layer=0` 또는 `layer=comp` 워터마크 이미지의 경우입니다. 마지막으로 대상 이미지에 대해 지정된 요청 및 보기 명령이 응답 이미지를 구성하기 위해 적용됩니다.

워터마크 이미지는 회신 이미지에 추가된 빈 공간을 `wid=` 및 `hei=` 명령.

## 예 {#section-0408c977d7324d4cb0e76a91cdfa2acd}

일반적인 워터마크는 로고나 저작권 알림이 포함된 간단한 RGBA 이미지로 구성될 수 있습니다. 이미지 카탈로그(또는 기본 카탈로그)에 `catalog::Id` 설정 `watermark` 워터마크 이미지 파일을 `catalog::Path`. 워터마크를 왜곡하지 않고 보기 이미지에 맞게 워터마크를 늘리려고 하며 약간의 여백을 추가로 남겨 두고 불투명도를 원래 워터마크의 20%로 줄여 설정하려고 합니다 `catalog::Modifier` to `sizeN=0.9,0.9&opac=20`. 워터마킹을 활성화하려면 `attribute::Watermark` 워터마크 카탈로그 항목의 id에 대해 이 예제에서는 &quot;watermark&quot;를 입력합니다. 우리는 다른 것을 실험하고 싶을 수 있습니다 `blendMode=` 다양한 워터마크 효과를 얻을 수 있는 선택 사항

## 참조 {#section-4d66713abacb42c7b6a0c93cbf966a97}

[속성::워터마크](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b)
