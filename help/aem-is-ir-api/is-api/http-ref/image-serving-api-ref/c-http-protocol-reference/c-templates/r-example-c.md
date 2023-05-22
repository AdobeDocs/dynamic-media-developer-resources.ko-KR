---
title: 예 C
description: '"종이 인형" 레이어 응용 프로그램을 만듭니다.'
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 70232055-2a4c-4e56-8076-3cd56a9004c5
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---

# 예 C{#example-c}

&quot;종이 인형&quot; 레이어 응용 프로그램을 만듭니다.

배경 이미지에는 모델 또는 마네킹의 사진이 포함되어 있습니다. 이미지 카탈로그의 추가 기록에는 마네킹의 모양과 크기에 맞게 촬영된 다양한 의류 및 액세서리 항목이 포함되어 있습니다.

각 의류/액세서리 사진은 이미지 크기를 최소화하기 위해 마스크 테두리 상자에 마스킹되고 잘립니다. 이미지 앵커와 해상도는 레이어와 배경 이미지 간의 정렬을 유지하도록 세심하게 제어되며, 모든 이미지는 적절한 값이에 저장된 상태로 이미지 카탈로그에 추가됩니다. `catalog::Resolution` 및 `catalog::Anchor`.

레이어 구성 외에도 선택한 항목의 색상을 변경할 수도 있습니다. 이러한 항목에 대한 레코드는 원래 색상을 제거하고 색상화 명령에 적합한 방식으로 명도와 대비를 조정하도록 사전 처리됩니다. 이 전처리는 Adobe Photoshop과 같은 이미지 편집 도구를 사용하여 오프라인에서 수행할 수도 있고, 간단한 경우 를 추가하여 소규모로 수행할 수도 있습니다 `op_brightness=` 및 `op_contrast=` (으)로 `catalog::Modifier`필드.

모든 개체가 이미지 앵커에 의해 이미 올바르게 정렬되었으므로 이 응용 프로그램에서는 별도의 템플릿을 사용할 수 없습니다( `catalog::Anchor`) 및 배율 조정( `catalog::Resolution`). 이는 적절한 레이어 순서를 보장하기 위해 클라이언트에 맡깁니다.

일반적인 요청은 다음과 같습니다.

```
http://server/rootId/mannequin?&hei=400&qlt=90&
layer=1&res=999&src=rootId/tankTopGeneric&colorize=240,122,17&
 layer=2&res=999&src=rootId/skirt14a&
layer=3&res=999&src=rootId/jacket09&
layer=4&res=999&src=rootId/hat2generic&colorize=12,15,34&
 layer=5&res=999&src=rootId/sunglasses&
layer=6&res=999&src=rootId/shoes21
```

높이만 지정됩니다. 이렇게 하면 배경색으로 여백을 채우지 않고도 마네킹 이미지의 종횡비에 따라 반환되는 이미지의 너비가 달라질 수 있습니다.

모든 해상도가 동일한 한 각 레이어에 대해 어떤 해상도가 지정되든 관계없습니다. 이 버전에서는 보기 수가 복합 이미지보다 크지 않을 수 있습니다. 큰 해상도 값을 지정하면 이 제한과 관련된 문제가 발생하지 않습니다. 모든 처리 및 합성은 최상의 성능 및 출력 품질을 달성하는 데 도움이 되도록 요청된 이미지 크기에 대한 최적의 해상도로 수행됩니다.

다음 `res=` 모든 소스 이미지의 해상도가 전체 스케일에서 동일하면 명령을 생략할 수 있습니다(이 유형의 응용 프로그램일 수 있음).

다음 `rootId` 은(는) 모두에 대해 지정해야 합니다. `src=` 명령(동일하더라도) `rootId` url 경로에 지정됩니다.

이미지 카탈로그를 사용할 필요가 없는 경우 해상도 기반의 크기 조정 접근 방식은 불가능합니다. 이 경우, 각 계층 항목별로 명시적 척도 요인을 의 비율에 기초하여 계산해야 한다. `catalog::Resolution` 각 레이어의 값을 `catalog::Resolution` 배경 레이어의 값입니다. 따라서 레이어 수가 적은 합성 요청은 다음과 같이 표시될 수 있습니다.

```
http://server/myApp/mannequin.tif?&hei=400&qlt=90&
 layer= 1&scale=0.3423&anchor=345,225&src=myApp/images/tankTopGeneric.tif&colorize=240,122,17&
 layer=2&scale=0.8544&anchor=140,-157&src=myApp/images/skirt14a
```
