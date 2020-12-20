---
description: req=img인 경우 합성 캔버스의 크기는 레이어 0의 크기에 의해 완전히 결정됩니다.
seo-description: req=img인 경우 합성 캔버스의 크기는 레이어 0의 크기에 의해 완전히 결정됩니다.
seo-title: 합성 캔버스
solution: Experience Manager
title: 합성 캔버스
topic: Scene7 Image Serving - Image Rendering API
uuid: 7ec2f1b3-61fc-4bfe-96d2-a5946a238e74
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 0%

---


# 합성 캔버스{#the-compositing-canvas}

req=img인 경우 합성 캔버스의 크기는 레이어 0의 크기에 의해 완전히 결정됩니다.

레이어 0에 대한 `size=`이 명시적으로 지정되지 않은 경우 레이어 변형을 사용하여 합성 캔버스의 크기를 계산합니다(아래 참조).

`req=tmb`인 경우 합성 캔버스의 크기는 레이어 0에 대해 지정된 `size=`에 의해 결정되거나, 크기가 지정되지 않은 경우 합성 캔버스 크기가 보기 레트로 설정됩니다(아래 참조).
