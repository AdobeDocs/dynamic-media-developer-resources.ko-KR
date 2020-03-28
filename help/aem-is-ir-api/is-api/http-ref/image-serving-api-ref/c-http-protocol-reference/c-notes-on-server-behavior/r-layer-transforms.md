---
description: 변환은 소스 이미지 및 텍스트 레이어에 적용됩니다.
seo-description: 변환은 소스 이미지 및 텍스트 레이어에 적용됩니다.
seo-title: 레이어 변형
solution: Experience Manager
title: 레이어 변형
topic: Scene7 Image Serving - Image Rendering API
uuid: b32b5af4-66ad-474a-9bca-4b6da8f43bf9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 레이어 변형{#layer-transforms}

변환은 소스 이미지 및 텍스트 레이어에 적용됩니다.

소스 이미지에 지정된 순서대로 다음 작업이 적용되어 레이어 0과 원하는 공간 관계를 이룰 수 있습니다.

1. 지정된 `crop=`경우 적용합니다.
1. 지정된 경우 `size=` 또는 지정되지 않은 경우, 기준이나 `size=` 지정되지 않은 경우, `scale=`또는 지정하지 않은 경우 전체 해상도 소스 이미지를 `scale=` `res=``res=`사용합니다.
1. 지정된 `flip=`경우 적용합니다.
1. 지정된 `rotate=`경우 적용합니다.
1. 지정된 `extend=`경우 적용합니다.
1. 및 를 기준으로 캔버스에 레이어를 `origin=` `pos=` 배치합니다(아래 참조).

다음 변형이 텍스트 레이어에 적용됩니다.

1. 텍스트 상자 크기는 `size=``size=` 부분적으로 제공되거나 전혀 제공되지 않을 경우 텍스트 너비와 높이로 결정됩니다. 텍스트 상자의 rtf 텍스트 정렬 특성을 사용하여 텍스트가 정렬됩니다. 텍스트 상자에 의해 텍스트가 잘릴 수 있습니다.
1. 로 지정된 해상도에 따라 텍스트 컨텐츠의 크기를 `textAttr=`조정합니다.
1. 지정된 `rotate=`경우 적용합니다.
1. 지정된 `extend=`경우 적용합니다.
1. 와 을 기준으로 캔버스에 레이어를 `origin=` 배치합니다(아래 참조). `pos=`

이미지 및 텍스트 레이어 모두에 대해 레이어 0이 캔버스를 효과적으로 구성하므로 캔버스에서 레이어의 마지막 위치를 조정할 때 레이어 0에는 적용되지 않습니다.
