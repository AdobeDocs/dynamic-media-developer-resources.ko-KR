---
description: 4가지 유형의 레이어가 지원됩니다.
seo-description: 4가지 유형의 레이어가 지원됩니다.
seo-title: 레이어 유형
solution: Experience Manager
title: 레이어 유형
topic: Scene7 Image Serving - Image Rendering API
uuid: d88b2163-7c9f-4885-9722-be3339e7127a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---


# 레이어 유형{#layer-types}

4가지 유형의 레이어가 지원됩니다.

## 이미지 레이어 {#section-3e53df1437694272aca03f927fc0db07}

이미지 레이어에는 레이어로 사용할 이미지를 지정하는 `src=` 명령이 있어야 합니다. 레이어 마스크로 사용할 별도의 이미지를 `mask=`으로 지정하거나 이미지에 이미 알파 채널이 있을 수 있습니다. 이미지 레이어의 크기는 항상 이미지에서 파생되지만, 이미지는 종종 `size=` 명령을 사용하여 크기에 맞게 조정됩니다. 클립 경로는 `clipPath=`과 함께 적용할 수 있습니다.

## 텍스트 레이어 {#section-dc2aec6416a340bcb20c1f884323c8d0}

텍스트 내용을 서식 있는 텍스트 형식(RTF) 텍스트 조각 형식으로 제공하는 `text=` 또는 `textPs=` 명령이 있어야 합니다. 텍스트 레이어는 내용에 맞게 크기를 조정할 수도 있고, 명확한 크기를 지정할 수도 있습니다(예를 들어, 텍스트를 특정 너비로 둘러싸야 하거나 특정 영역 내에서 텍스트를 제한해야 하는 경우). `textPs=` 로 정의된 임의 패스로 정의된 임의 모양 `textFlowPath=` 으로 텍스트를 이동하는  `textPath=`지원 `textPs=` 또한 텍스트 상자에 텍스트를 렌더링하거나 임의의 각도(  `textAngle=`)로 지정된 모양을 렌더링할 수 있습니다.

## 단색 레이어 {#section-56dfb672756643dda08dc93294809eb0}

단색 레이어는 템플릿에서 레이어 0에 주로 사용되므로 합성 이미지의 크기가 고정되고 이미지 컨텐츠와 독립적입니다. 단색 레이어는 `color=` 속성과 `size=` 또는 `mask=` 중 하나를 필요로 하며, 모양을 수정할 대부분의 다른 명령 및 특성을 지원합니다. 단색 레이어에는 `clipPath=`의 임의 모양이 지정될 수 있습니다.

## 효과 레이어 {#section-dd3b628bc6734077af4c0ddcebcee05f}

그림자 및 광선 효과와 같은 Photoshop 스타일 레이어 효과는 이미지, 텍스트 및 단색 레이어에 첨부할 수 있는 특수 하위 레이어를 사용하여 IS에서 구현됩니다. 이러한 효과 레이어는 상위 레이어에서 상위 레이어 마스크와 위치를 상속하며, 기능이 제한됩니다.
