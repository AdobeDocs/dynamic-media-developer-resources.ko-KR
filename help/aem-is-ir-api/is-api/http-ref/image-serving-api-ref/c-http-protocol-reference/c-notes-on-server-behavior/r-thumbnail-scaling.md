---
description: '이미지 레이어 변형 2단계는 축소판의 다음과 같이 수정됩니다(예: req=tmb).'
seo-description: '이미지 레이어 변형 2단계는 축소판의 다음과 같이 수정됩니다(예: req=tmb).'
seo-title: 축소판 크기 조정
solution: Experience Manager
title: 축소판 크기 조정
topic: Dynamic Media Image Serving - Image Rendering API
uuid: df935d40-84c6-4018-9e41-faef4653ff1f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---


# 축소판 크기 조절{#thumbnail-scaling}

이미지 레이어 변형 2단계는 축소판의 다음과 같이 수정됩니다(예: req=tmb).

* `2.` 지정된  `size=` 경우 축소판 규칙을 사용하여 이미지 `size=` 를 최신 위치에 맞추십시오. `size=`이 지정되지 않은 경우 `res=`을 기준으로 크기를 조정하거나, `res=`이 지정되지 않은 경우, 아래에 나와 있는 축소판 규칙을 사용하여 캔버스 오른쪽에 잘린 이미지를 맞추십시오.

