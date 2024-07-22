---
description: 이미지 제공은 간단한 시각적 워터마크 기능을 구현합니다.
solution: Experience Manager
title: 워터마크
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e744be3f-9753-4513-8f37-055fa03077cc
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 0%

---

# 워터마크{#watermarks}

이미지 제공은 간단한 시각적 워터마크 기능을 구현합니다.

워터마크는 일반적으로 반투명 이미지이지만 텍스트 또는 보다 복잡하고 계층화된 합성 이미지일 수 있습니다. 모든 보기 특성(`wid=`, `hei=`, `align=`, `scl=`, `bgc=`)이 적용된 후 서버에서 응답 이미지 위에 워터마크를 계층화합니다.

워터마크 이미지 또는 템플릿을 포함하는 올바른 카탈로그 항목으로 `attribute::Watermark`을(를) 설정하여 워터마킹을 사용할 수 있습니다. `attribute::Watermark`이(가) 명명된 카탈로그에 설정된 경우 서버는 요청 URL에서 카탈로그 ID를 참조하는 모든 이미지 요청에 워터마크를 추가합니다. `default::Watermark`이(가) 설정된 경우(기본 카탈로그: [!DNL default.ini]), 워터마크가 카탈로그를 참조하는지 여부에 관계없이 모든 이미지 요청에 적용됩니다.

썸네일 요청(`req=tmb`) 및 Dynamic Media 뷰어의 특정 요청에 대한 응답으로 반환된 이미지에는 워터마크가 적용되지 않습니다.

## 크기 조절 및 정렬 {#section-89ef9e5926ae438abbd8e70332749b76}

워터마크가 지정되면 서버는 먼저 뷰변환을 적용하기 전에 워터마크를 적용해야 하는 합성 이미지(*대상 이미지*)를 생성합니다. 그런 다음 서버는 다른 이미지(*워터마크 이미지*)와 마찬가지로 워터마크에 대한 합성 이미지를 생성합니다.

표준 이미지와 달리 워터마크 이미지의 layer=0 또는 layer=comp에 대해 `sizeN=`을(를) 지정할 수 있습니다. 대상 이미지를 기준으로 워터마크 이미지의 크기를 조정할 수 있습니다. `sizeN=`을(를) 지정하지 않으면 대상 이미지와 병합될 때 워터마크 이미지의 픽셀 크기가 유지됩니다.

워터마크 레코드에서 요청 명령(예: `fmt=`) 및 보기 명령(예: `wid=`)은 무시됩니다. 단, `align=`은(는) 예외입니다. `align=`을(를) 사용하여 대상 이미지를 기준으로 워터마크 이미지를 상대적으로 배치할 수 있습니다. 이것은 타겟 이미지의 코너 또는 에지에 대한 워터마크의 위치를 허용한다.

크기 조절 및 정렬 후 서버는 워터마크 이미지의 `layer=0` 또는 `layer=comp`에 대해 지정된 `blendMode=` 및 `opac=` 값을 사용하여 대상 이미지 위에 워터마크 이미지를 계층화합니다. 마지막으로, 타겟 이미지에 대해 지정된 요청 및 뷰 명령이 적용되어 응답 이미지를 구성한다.

워터마크 이미지는 `wid=` 및 `hei=` 명령으로 응답 이미지에 추가된 빈 공백에 확장되지 않습니다.

## 예 {#section-0408c977d7324d4cb0e76a91cdfa2acd}

일반적인 워터마크는 로고 또는 저작권 표시가 포함된 간단한 RGBA 이미지로 구성될 수 있습니다. `catalog::Id`이(가) `watermark`(으)로 설정된 이미지 카탈로그(또는 기본 카탈로그)에 레코드를 만들고 `catalog::Path`에 워터마크 이미지 파일을 지정합니다. 여백을 약간 남겨두고 워터마크를 보기 이미지에 맞게 늘리고(워터마크를 왜곡하지 않고) 불투명도를 원래 워터마크의 20%로 줄이려고 하므로 `catalog::Modifier`을(를) `sizeN=0.9,0.9&opac=20`(으)로 설정합니다. 워터마킹을 활성화하려면 이 예제에서 `attribute::Watermark`을(를) 워터마크 카탈로그 항목의 ID &quot;watermark&quot;로 설정합니다. 다양한 워터마크 효과를 얻기 위해 다양한 `blendMode=` 선택 사항을 실험해 볼 수 있습니다.

## 참조 {#section-4d66713abacb42c7b6a0c93cbf966a97}

[속성::워터마크](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b)
