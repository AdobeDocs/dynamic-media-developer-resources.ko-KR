---
description: '이미지 레이어 변환의 2단계는 축소판의 경우 다음과 같이 수정됩니다(예: req=tmb).'
seo-description: '이미지 레이어 변환의 2단계는 축소판의 경우 다음과 같이 수정됩니다(예: req=tmb).'
seo-title: 축소판 크기 조정
solution: Experience Manager
title: 축소판 크기 조정
topic: Scene7 Image Serving - Image Rendering API
uuid: df935d40-84c6-4018-9e41-faef4653ff1f
translation-type: tm+mt
source-git-commit: 87164dbf805a179f7bdeecd7cc6140c3456b61bb

---


# 축소판 크기 조정{#thumbnail-scaling}

이미지 레이어 변환의 2단계는 축소판의 경우 다음과 같이 수정됩니다(예: req=tmb).

* `2.` 지정된 `size=` 경우 축소판 규칙을 사용하여 잘려진 이미지를 `size=` 다시 맞추십시오. 지정하지 `size=` 않으면 크기를 `res=`기준으로 조정하거나 지정하지 `res=` 않으면 아래 나와 있는 축소판 규칙을 사용하여 잘려진 이미지를 캔버스 끝에 맞추십시오.

