---
description: 4가지 일반적인 유형의 제작 비네팅이 지원됩니다.
solution: Experience Manager
title: 비네팅 크기 조절
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f9f92254-41d8-4d22-a168-78b49dd55478
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# 비네팅 크기 조절{#vignette-scaling}

4가지 일반적인 유형의 제작 비네팅이 지원됩니다.

* 단일 해상도

  단일 렌더링 이미지 크기만 필요한 것이 확실한 경우에만 권장됩니다.
* 다중 해상도

  원하는 모든 렌더링 이미지 크기를 알고 있는 경우에 권장됩니다. 렌더링 후 이미지 크기를 조정할 필요가 없으므로 단일 해상도 및 피라미드 비네팅보다 더 나은 품질과 더 빠른 렌더링을 제공합니다.
* 피라미드형

  여러 이미지 크기가 필요하고 정확한 크기가 미리 결정되지 않은 경우 및 Dynamic Media 확대/축소 뷰어를 사용하는 경우에 가장 적합한 것이 좋습니다.
* 하나 이상의 추가 해상도가 있는 피라미드형

  특정 크기에 맞는 고품질을 제공하면서도 여전히 유연성과 확대/축소 뷰어 지원을 제공합니다.

효과적으로 각 해상도는 자체 이미지 폭과 높이를 갖는 독립 보기로 프로덕션 비네팅에 저장됩니다.

단일 해상도 비네팅의 보기 크기가 `-width` 또는 `-height` 중 하나 또는 둘 다로 지정되었습니다. 두 값을 모두 지정하면 두 차원 모두 지정된 크기보다 크지 않도록 비네팅의 크기가 조정됩니다. 두 값 모두 지정하지 않으면 출력 비네팅의 크기가 입력 비네팅의 크기와 같습니다. 업스케일링이 적용되지 않습니다. 지정된 크기가 입력 비네팅의 크기보다 큰 경우 출력 비네팅의 크기는 입력 비네팅과 동일합니다.

첫 번째 해상도 수준이 단일 해상도 비네팅과 같은 크기가 되면서 여러 해상도 비네팅에는 동일한 규칙이 효과적으로 적용됩니다. 추가 해상도는 `-width` 또는 `-height`에 대해 추가로 쉼표로 구분된 값으로 지정됩니다. 값을 정렬할 필요가 없습니다. `-width`이(가) 여러 값을 지정하는 경우 `-height`은(는) 단일 값만 제공해야 하며 그 반대의 경우도 마찬가지입니다. 그렇지 않으면 오류가 반환됩니다.

`-pyramid`을(를) 지정하여 피라미드형 비네팅을 만듭니다. 이러한 비네팅의 최대 해상도 레벨은 단일 해상도 비네팅에 대한 것과 정확히 동일하게 결정된다. 추가 해상도 수준은 각 수준을 이전 수준의 0.5배 크기로 조정하여 자동으로 결정되며, 가장 작은 수준은 128x128픽셀을 초과하지 않습니다.

다중 해상도 비네팅의 경우와 마찬가지로 피라미드 비네팅에 대해서도 추가적인 해상도 레벨을 지정할 수 있다.
