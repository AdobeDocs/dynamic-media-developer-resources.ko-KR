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

---


# 합성 캔버스{#the-compositing-canvas}

req=img인 경우 합성 캔버스의 크기는 레이어 0의 크기에 의해 완전히 결정됩니다.

레이어 0 `size=` 에 대해 명시적으로 지정하지 않으면 레이어 변형 기능을 사용하여 합성 캔버스의 크기를 계산합니다(아래 참조).

합성 `req=tmb`캔버스의 크기는 레이어 0에 대해 `size=` 지정된 크기로 결정되거나, 크기를 지정하지 않으면 합성 캔버스 크기가 보기 음성으로 설정됩니다(아래 참조).
