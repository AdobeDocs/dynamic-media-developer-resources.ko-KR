---
description: 레이어 원점(원본=)을 배경 레이어 원점과 함께 pos=로 지정된 오프셋에 맞춰 레이어를 배치합니다.
solution: Experience Manager
title: 레이어 배치
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 0%

---


# 레이어 배치{#layer-placement}

레이어 원점(원본=)을 배경 레이어 원점과 함께 pos=로 지정된 오프셋에 맞춰 레이어를 배치합니다.

레이어 원점을 이미지 레이어에 명시적으로 지정하지 않으면 다음과 같이 계산됩니다.

1. 이미지 앵커를 결정합니다. `anchor=` 또는 지정하지 않은 경우 `catalog::Anchor`을 사용합니다.
1. 이미지 앵커가 정의된 경우 레이어 변형 및 `extend=`을 적용하여 원본= 값으로 변환합니다.
1. 이미지 앵커가 정의되지 않은 경우 레이어 원점은 레이어 사각형 중앙에 배치됩니다(`extend=` 적용 후).

![](assets/layerplacement.png)

