---
description: 네 가지 유형의 레이어가 지원됩니다.
solution: Experience Manager
title: 레이어 유형
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9819a73d-1108-414a-831f-37ba94c3feb9
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---

# 레이어 유형{#layer-types}

네 가지 유형의 레이어가 지원됩니다.

## 이미지 레이어 {#section-3e53df1437694272aca03f927fc0db07}

이미지 레이어에는 `src=` 레이어로 사용할 이미지를 지정하는 명령입니다. 별도의 이미지를 `mask=` 레이어 마스크 또는 이미지로 사용할 경우 이미 알파 채널이 있을 수 있습니다. 이미지 레이어의 크기는 항상 이미지에서 파생되지만 이미지를 사용하여 크기에 맞게 조정하는 경우가 많습니다 `size=` 명령입니다. 클립 경로는 다음과 같이 적용될 수 있습니다. `clipPath=`.

## 텍스트 레이어 {#section-dc2aec6416a340bcb20c1f884323c8d0}

은(는) 을(를) 포함해야 합니다. `text=` 또는 `textPs=` rich-text-formatted (RTF) 텍스트 조각 형식으로 텍스트 콘텐츠를 제공하는 명령입니다. 텍스트 레이어는 내용에 맞게 자체 크기가 조정되거나 명확한 크기가 주어질 수 있습니다. 예를 들어, 텍스트를 특정 너비로 줄바꿈해야 하는 경우 또는 텍스트를 특정 영역 내에서 제한해야 하는 경우입니다. `textPs=` 다음을 사용하여 정의된 임의의 도형으로 텍스트 흐름 지원 `textFlowPath=` 을 사용하여 정의된 임의의 경로로 `textPath=`. `textPs=` 또한 텍스트 상자 또는 지정된 셰이프에 텍스트를 임의의 각도로 렌더링할 수 있습니다( `textAngle=`).

## 단색 레이어 {#section-56dfb672756643dda08dc93294809eb0}

단색 레이어는 종종 템플릿의 레이어 0에 사용되므로 합성 이미지의 크기가 이미지 내용에 관계없이 고정되어 있습니다. 단색 레이어에는 `color=` 속성 및 `size=` 또는 `mask=`및 에서는 대부분의 다른 명령과 속성을 지원하여 모양을 수정할 수 있습니다. 단색 레이어에는 `clipPath=`.

## 효과 레이어 {#section-dd3b628bc6734077af4c0ddcebcee05f}

그림자 및 광선 효과와 같은 Photoshop 스타일 레이어 효과는 이미지, 텍스트 및 단색 레이어에 첨부할 수 있는 특수 하위 레이어를 사용하여 IS에 의해 구현됩니다. 이러한 효과 레이어는 상위 레이어에서 상위 레이어 마스크와 위치를 상속하며 기능이 제한됩니다.
