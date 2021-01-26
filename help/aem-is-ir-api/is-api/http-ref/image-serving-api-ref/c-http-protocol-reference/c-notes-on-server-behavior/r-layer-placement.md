---
description: 레이어 원점(원본=)을 배경 레이어 원점과 함께 pos=로 지정된 오프셋에 맞춰 레이어를 배치합니다.
seo-description: 레이어 원점(원본=)을 배경 레이어 원점과 함께 pos=로 지정된 오프셋에 맞춰 레이어를 배치합니다.
seo-title: 레이어 배치
solution: Experience Manager
title: 레이어 배치
topic: Dynamic Media Image Serving - Image Rendering API
uuid: d9d778f2-13dd-4ea1-a703-52eac70bb3d8
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 0%

---


# 레이어 배치{#layer-placement}

레이어 원점(원본=)을 배경 레이어 원점과 함께 pos=로 지정된 오프셋에 맞춰 레이어를 배치합니다.

레이어 원점을 이미지 레이어에 명시적으로 지정하지 않으면 다음과 같이 계산됩니다.

1. 이미지 앵커를 결정합니다. `anchor=` 또는 지정하지 않은 경우 `catalog::Anchor`을 사용합니다.
1. 이미지 앵커가 정의된 경우 레이어 변형 및 `extend=`을 적용하여 원본= 값으로 변환합니다.
1. 이미지 앵커가 정의되지 않은 경우 레이어 원점은 레이어 사각형 중앙에 배치됩니다(`extend=` 적용 후).

![](assets/layerplacement.png)

