---
description: 이미지 제공 서비스는 간단한 시각적 워터마크 기능을 구현합니다.
solution: Experience Manager
title: 워터마크
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e744be3f-9753-4513-8f37-055fa03077cc
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 1%

---

# 워터마크{#watermarks}

이미지 제공 서비스는 간단한 시각적 워터마크 기능을 구현합니다.

워터마크는 일반적으로 반투명 이미지만 텍스트일 수도 있고 더 복잡한 레이어 복합 이미지입니다. 모든 보기 특성( `wid=`, `hei=`, `align=`, `scl=`, `bgc=`)이 적용된 후 서버에서 회신 이미지 위에 워터마크를 레이어에 지정합니다.

워터마크는 워터마크 이미지나 템플릿을 포함하는 유효한 카탈로그 항목으로 `attribute::Watermark`을 설정하여 사용할 수 있습니다. 명명된 카탈로그에서 `attribute::Watermark`가 설정된 경우 서버는 요청 URL에서 카탈로그 ID를 참조하는 모든 이미지 요청에 워터마크를 추가합니다. `default::Watermark` 이 설정된 경우(기본 카탈로그의 [!DNL default.ini]), 워터마크가 카탈로그를 참조하는지 여부에 관계없이 모든 이미지 요청에 적용됩니다.

워터마크는 Dynamic Media 뷰어의 축소판 요청( `req=tmb`) 및 특정 요청에 응답하여 반환되는 이미지에 적용되지 않습니다.

## 크기 조절 및 정렬 {#section-89ef9e5926ae438abbd8e70332749b76}

워터마크를 지정하면 서버가 먼저 워터마크를 적용해야 하는 합성 이미지(*대상 이미지*)를 생성합니다(보기 변형을 적용하기 전에). 그러면 서버는 다른 이미지와 마찬가지로 워터마크의 합성 이미지를 생성합니다( *워터마크 이미지*).

표준 이미지와는 달리 `sizeN=`은(는) layer=0 또는 layer=comp에 대해 지정할 수 있습니다. 이를 통해 대상 이미지를 기준으로 워터마크 이미지의 크기를 조정할 수 있습니다. `sizeN=`을 지정하지 않으면 대상 이미지와 병합될 때 워터마크 이미지가 픽셀 크기를 유지합니다.

`align=`를 제외하고 워터마크 레코드에서는 요청 명령(예: `fmt=`) 및 보기 명령(예: `wid=`)이 무시됩니다. `align=` 대상 이미지를 기준으로 하여 워터마크 이미지를 배치하기 위해 사용할 수 있습니다. 이를 통해 대상 이미지의 모서리나 모서리에 대해 워터마크 위치를 지정할 수 있습니다.

크기 조절 및 정렬 후에 서버는 워터마크 이미지의 `blendMode=` 및 `layer=0` 또는 `layer=comp`에 대해 지정된 `opac=` 값을 사용하여 대상 이미지 위에 워터마크 이미지를 레이어에 지정합니다. 마지막으로 대상 이미지에 대해 지정된 요청 및 보기 명령이 응답 이미지를 구성하기 위해 적용됩니다.

워터마크 이미지는 `wid=` 및 `hei=` 명령에 의해 응답 이미지에 추가된 빈 공간을 초과하지 않습니다.

## 예 {#section-0408c977d7324d4cb0e76a91cdfa2acd}

일반적인 워터마크는 로고나 저작권 알림이 포함된 간단한 RGBA 이미지로 구성될 수 있습니다. 이미지 카탈로그(또는 기본 카탈로그)에 `catalog::Id`이 `watermark`로 설정된 레코드를 만들고 `catalog::Path`에 워터마크 이미지 파일을 지정합니다. 워터마크를 왜곡하지 않고 보기 이미지에 맞게 워터마크를 늘리려고 하며 약간 여백을 더 작게 유지하고 불투명도를 원래 워터마크의 20%로 줄이므로 `catalog::Modifier`을 `sizeN=0.9,0.9&opac=20`로 설정하려고 합니다. 워터마킹을 활성화하려면 이 예에서 `attribute::Watermark`을 워터마크 카탈로그 항목의 ID로 설정합니다. 다른 `blendMode=` 선택 항목을 실험해 보고 다른 워터마크 효과를 얻을 수 있습니다.

## 참조 {#section-4d66713abacb42c7b6a0c93cbf966a97}

[속성::워터마크](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b)
