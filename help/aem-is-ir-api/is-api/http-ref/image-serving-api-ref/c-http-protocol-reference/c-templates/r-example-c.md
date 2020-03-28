---
description: '"종이 인형" 레이어 애플리케이션을 만듭니다.'
seo-description: '"종이 인형" 레이어 애플리케이션을 만듭니다.'
seo-title: 예 C
solution: Experience Manager
title: 예 C
topic: Scene7 Image Serving - Image Rendering API
uuid: 25f228c2-dc03-461a-aee8-40fdb3d4cf5e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 예 C{#example-c}

&quot;종이 인형&quot; 레이어 애플리케이션을 만듭니다.

배경 이미지에는 모델 또는 마네킹의 사진이 포함되어 있습니다. 이미지 카탈로그의 추가 기록에는 모양과 크기의 마네킹에 맞게 촬영한 다양한 의류와 액세서리 항목이 포함되어 있습니다.

각 의류/액세서리 사진은 마스크 처리 및 마스크 테두리 상자로 잘려 이미지 크기를 최소화합니다. 이미지 앵커 및 해상도는 레이어와 배경 이미지 간의 정렬을 유지하기 위해 신중하게 제어되며, 모든 이미지가 이미지 카탈로그에 추가되고 `catalog::Resolution` 및 에 적절한 값이 `catalog::Anchor`저장됩니다.

레이어링 외에도 선택한 항목의 색상을 변경하려고 합니다. 이러한 항목의 레코드는 원래 색상을 제거하고 색상화 명령에 적합한 방식으로 밝기와 대비를 조정하기 위해 미리 처리됩니다. 이 사전 처리는 Photoshop과 같은 이미지 편집 도구를 사용하여 오프라인으로 하거나, 간단한 경우 `op_brightness=` 필드에 추가 및 `op_contrast=` `catalog::Modifier`추가하여 세밀하게 수행할 수 있습니다.

모든 개체가 이미 이미지 앵커()로 정렬되고 크기 조절()되어 있으므로 이 응용 프로그램은 별도의 템플릿을 보장하지 않습니다. `catalog::Anchor``catalog::Resolution` 적절한 레이어 순서를 위해 고객에게 보관합니다.

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

높이만 지정됩니다. 이렇게 하면 배경색으로 여백을 채우지 않고도 반환된 이미지의 종횡비에 따라 너비가 달라질 수 있습니다.

모든 레이어가 동일한 경우 각 레이어에 대해 어떤 해상도를 지정하더라도 상관없습니다. 이 버전에서는 보기가 합성 이미지보다 클 수 없습니다. 큰 해상도 값을 지정하면 이 제한 사항과 관련된 문제가 방지됩니다. 모든 처리 및 합성은 요청된 이미지 크기에 대한 최적의 해상도로 수행되므로 최상의 성능과 출력 품질을 얻을 수 있습니다.

모든 소스 이미지의 해상도가 전체 크기(이 유형의 응용 프로그램의 경우일 수 있음)에 동일한 경우 명령을 생략할 수 있습니다. `res=`

URL 경로에 `rootId` 지정된 명령과 동일한 경우에도 모든 `src=` `rootId` 명령에 대해 URL을 지정해야 합니다.

이미지 카탈로그를 사용할 수 없는 경우 해상도를 기반으로 크기 조정을 할 수 없습니다. 이 경우 각 레이어 항목에 대해 배경 레이어의 값에 대한 `catalog::Resolution` 값의 비율을 기준으로 명확한 비율 요소를 `catalog::Resolution` 계산해야 합니다. 따라서 합성 요청(레이어 수 감소)은 다음과 같습니다.

```
http://server/myApp/mannequin.tif?&hei=400&qlt=90&
 layer= 1&scale=0.3423&anchor=345,225&src=myApp/images/tankTopGeneric.tif&colorize=240,122,17&
 layer=2&scale=0.8544&anchor=140,-157&src=myApp/images/skirt14a
```

