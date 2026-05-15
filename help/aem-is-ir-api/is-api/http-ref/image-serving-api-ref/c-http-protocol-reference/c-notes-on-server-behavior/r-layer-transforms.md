---
description: 변형은 소스 이미지와 텍스트 레이어에 적용됩니다.
solution: Experience Manager
title: 레이어 변형
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5758d07c-bb84-4ab1-bf77-f59cf93f5e90
TQID: 'https://experienceleague.adobe.com/jChFcZzWWOlbicpu0WeRSJb608dGT9JmVSItV-uEjBY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 201
ht-degree: 0%

---

# 레이어 변형{#layer-transforms}

변형은 소스 이미지와 텍스트 레이어에 적용됩니다.

레이어 0과의 원하는 공간 관계를 달성하기 위해 다음 작업이 지정된 순서로 소스 이미지에 적용됩니다.

1. 지정된 경우 `crop=`을(를) 적용합니다.
1. `size=`을(를) 기반으로 크기 조절 또는 `size=`을(를) 지정하지 않은 경우 `scale=`을(를) 기반으로 크기 조절 또는 `scale=`을(를) 지정하지 않은 경우 `res=`을(를) 기반으로 크기 조절 또는 `res=`을(를) 지정하지 않은 경우 전체 해상도 소스 이미지를 사용합니다.
1. 지정된 경우 `flip=`을(를) 적용합니다.
1. 지정된 경우 `rotate=`을(를) 적용합니다.
1. 지정된 경우 `extend=`을(를) 적용합니다.
1. `origin=` 및 `pos=`을(를) 기준으로 캔버스에 레이어를 배치합니다(아래 참조).

텍스트 레이어에는 다음과 같은 변형이 적용됩니다.

1. 텍스트 상자 크기는 `size=` 또는 `size=`이(가) 일부만 제공되거나 전혀 제공되지 않는 경우 텍스트 너비 및 높이에 따라 결정됩니다. rtf 텍스트 정렬 속성을 사용하여 텍스트 상자 내에서 텍스트를 정렬합니다. 텍스트 상자에 의해 텍스트가 잘릴 수 있습니다.
1. `textAttr=`(으)로 지정된 해상도에 따라 텍스트 콘텐츠의 크기를 조정합니다.
1. 지정된 경우 `rotate=`을(를) 적용합니다.
1. 지정된 경우 `extend=`을(를) 적용합니다.
1. `origin=` 및 `pos=`을(를) 기준으로 캔버스에 레이어를 배치합니다(아래 참조).

이미지 레이어와 텍스트 레이어 모두 레이어 0이 캔버스를 효과적으로 구성하므로 캔버스에서 레이어를 마지막으로 배치한 단계는 레이어 0에 적용되지 않습니다.
