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

배경 이미지에는 모델이나 마네킹의 사진이 포함되어 있습니다. 이미지 카탈로그의 추가 레코드에는 모양과 크기의 마네킹에 맞게 촬영된 다양한 의류와 액세서리 항목이 포함되어 있습니다.

각 의복/액세서리 사진은 마스크되고 이미지 크기를 최소화하기 위해 마스크 테두리 상자에 잘립니다. 이미지 앵커와 해상도는 레이어와 배경 이미지 간의 정렬을 유지하기 위해 신중하게 제어되며, 모든 이미지는 `catalog::Resolution` 및 `catalog::Anchor`에 저장된 적절한 값으로 이미지 카탈로그에 추가됩니다.

계층화 외에 선택한 항목의 색상을 변경할 수도 있습니다. 이러한 항목의 레코드는 원래 색상을 제거하고 색화 명령에 적합한 방식으로 밝기와 대비를 조절하도록 미리 처리됩니다. 이 사전 처리는 Adobe Photoshop과 같은 이미지 편집 도구를 사용하여 오프라인에서 수행하거나, 간단한 경우 `op_brightness=` 및 `op_contrast=`을 `catalog::Modifier`필드에 추가하여 세 가지 방식으로 수행할 수 있습니다.

모든 개체가 이미 이미지 앵커( `catalog::Anchor`)에 의해 정렬되고 크기가 조정된( `catalog::Resolution`)이기 때문에 이 응용 프로그램은 별도의 템플릿을 보장하지 않습니다. 적절한 레이어 순서를 위해 클라이언트에 맡겨 둡니다.

일반적인 요청은 다음과 같을 수 있습니다.

```
http://server/rootId/mannequin?&hei=400&qlt=90&
layer=1&res=999&src=rootId/tankTopGeneric&colorize=240,122,17&
 layer=2&res=999&src=rootId/skirt14a&
layer=3&res=999&src=rootId/jacket09&
layer=4&res=999&src=rootId/hat2generic&colorize=12,15,34&
 layer=5&res=999&src=rootId/sunglasses&
layer=6&res=999&src=rootId/shoes21
```

높이만 지정됩니다. 이렇게 하면 배경색으로 채워진 여백을 가져오지 않고 반환된 이미지가 마네킹 이미지의 종횡비에 따라 너비가 달라질 수 있습니다.

각 레이어의 해상도가 모두 동일한 경우 어떤 해상도를 지정해도 안 됩니다. 이 버전에서는 보기가 복합 이미지보다 클 수 없습니다. 큰 해상도 값을 지정하면 이 제한 사항과 관련된 문제가 발생하지 않습니다. 모든 처리 및 합성은 요청된 이미지 크기에 대한 최적의 해상도로 수행되므로 최상의 성능과 출력 품질을 얻을 수 있습니다.

모든 소스 이미지의 해상도가 전체 크기(이 유형의 응용 프로그램의 경우일 수 있음)로 동일한 경우 `res=` 명령을 생략할 수 있습니다.

`rootId` 명령은 URL 경로에 지정된 `rootId` 명령과 동일한 경우에도 모든 `src=` 명령에 대해 지정해야 합니다.

이미지 카탈로그를 사용할 필요가 없는 경우에는 해상도 기반의 크기 조절 방법을 사용할 수 없습니다. 이 경우 배경 레이어의 `catalog::Resolution` 값에 대한 각 레이어의 `catalog::Resolution` 값의 비율을 기준으로 각 레이어 항목에 대해 명시적 배율 계수를 계산해야 합니다. 따라서 합성 요청(레이어 수가 적음)은 다음과 같을 수 있습니다.

```
http://server/myApp/mannequin.tif?&hei=400&qlt=90&
 layer= 1&scale=0.3423&anchor=345,225&src=myApp/images/tankTopGeneric.tif&colorize=240,122,17&
 layer=2&scale=0.8544&anchor=140,-157&src=myApp/images/skirt14a
```
