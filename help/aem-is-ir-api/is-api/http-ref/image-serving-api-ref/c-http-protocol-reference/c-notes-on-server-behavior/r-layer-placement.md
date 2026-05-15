---
title: 레이어 배치
escription: Layers are positioned by aligning the layer origin (origin=) with the background layer origin at an offset specified by pos=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1ce7bef3-a0f8-44fc-a146-7e819c30eee8
TQID: https://experienceleague.adobe.com/SMf4V0AmxYIi0o0FZhMkRx9pprIxjJjEcCWT2agF1Bo
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 0f5947b3f28ba40cd479df463c843f7e99155d5e
workflow-type: tm+mt
source-wordcount: 91
ht-degree: 0%

---

# 레이어 배치{#layer-placement}

레이어 원점(origin=)을 pos=에 의해 지정된 오프셋에 배경 레이어 원점과 정렬하여 레이어를 배치합니다.

이미지 레이어에 대해 레이어 원점을 명시적으로 지정하지 않으면 다음과 같이 계산됩니다.

1. 이미지 앵커를 결정합니다. `anchor=`을(를) 사용하거나 지정하지 않은 경우 `catalog::Anchor`을(를) 사용합니다.
1. 이미지 앵커가 정의된 경우 레이어 변환 및 `extend=`을(를) 적용하여 origin= 값으로 변환합니다.
1. 이미지 앵커가 정의되지 않은 경우 레이어 원점은 레이어 사각형의 중심에 배치됩니다(`extend=` 적용 후).

![레이어 배치 이미지](assets/layerplacement.png)
