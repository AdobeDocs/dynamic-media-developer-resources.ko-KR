---
title: 레이어 배치
escription: Layers are positioned by aligning the layer origin (origin=) with the background layer origin at an offset specified by pos=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1ce7bef3-a0f8-44fc-a146-7e819c30eee8
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---

# 레이어 배치{#layer-placement}

레이어 원점(origin=)을 pos=에 의해 지정된 오프셋에 배경 레이어 원점과 정렬하여 레이어를 배치합니다.

이미지 레이어에 대해 레이어 원점을 명시적으로 지정하지 않으면 다음과 같이 계산됩니다.

1. 이미지 앵커를 결정합니다. `anchor=`을(를) 사용하거나 지정하지 않은 경우 `catalog::Anchor`을(를) 사용합니다.
1. 이미지 앵커가 정의된 경우 레이어 변환 및 `extend=`을(를) 적용하여 origin= 값으로 변환합니다.
1. 이미지 앵커가 정의되지 않은 경우 레이어 원점은 레이어 사각형의 중심에 배치됩니다(`extend=` 적용 후).

![레이어 배치 이미지](assets/layerplacement.png)
