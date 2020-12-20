---
description: 변형 효과는 소스 이미지 및 텍스트 레이어에 적용됩니다.
seo-description: 변형 효과는 소스 이미지 및 텍스트 레이어에 적용됩니다.
seo-title: 레이어 변형
solution: Experience Manager
title: 레이어 변형
topic: Scene7 Image Serving - Image Rendering API
uuid: b32b5af4-66ad-474a-9bca-4b6da8f43bf9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---


# 레이어 변형{#layer-transforms}

변형 효과는 소스 이미지 및 텍스트 레이어에 적용됩니다.

다음 작업은 지정된 순서로 소스 이미지에 적용되어 레이어 0과 원하는 공간 관계를 만듭니다.

1. 지정한 경우 `crop=`을 적용합니다.
1. `size=` 또는 `size=`을 기준으로 `scale=`을(를) 지정하지 않았거나 `res=`을 기준으로 `scale=`이 지정되지 않았거나 `res=`가 지정되지 않은 경우 전체 해상도 소스 이미지를 사용합니다.
1. 지정한 경우 `flip=`을 적용합니다.
1. 지정한 경우 `rotate=`을 적용합니다.
1. 지정한 경우 `extend=`을 적용합니다.
1. `origin=` 및 `pos=`을 기준으로 캔버스에 레이어를 배치합니다(아래 참조).

텍스트 레이어에는 다음과 같은 변형이 적용됩니다.

1. 텍스트 상자 크기는 `size=` 또는 `size=`이 일부만 제공되거나 전혀 제공되지 않을 경우 텍스트 너비와 높이에 의해 결정됩니다. 텍스트가 텍스트 상자 내에서 rtf 텍스트 정렬 특성을 사용하여 정렬됩니다. 텍스트를 텍스트 상자로 자를 수 있습니다.
1. `textAttr=`으로 지정된 해상도에 따라 텍스트 내용의 크기를 조정합니다.
1. 지정한 경우 `rotate=`을 적용합니다.
1. 지정한 경우 `extend=`을 적용합니다.
1. `origin=` 및 `pos=`(아래 참조)을 기준으로 캔버스에 레이어를 배치합니다.

이미지 레이어와 텍스트 레이어 모두에 대해 레이어 0이 캔버스를 효과적으로 구성하므로 캔버스에서 레이어의 마지막 단계 위치를 지정할 때 레이어 0에는 적용되지 않습니다.
