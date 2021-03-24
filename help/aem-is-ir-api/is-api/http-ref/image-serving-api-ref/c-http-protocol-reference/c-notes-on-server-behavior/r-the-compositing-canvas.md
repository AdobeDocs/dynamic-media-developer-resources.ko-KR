---
description: req=img인 경우 합성 캔버스의 크기는 레이어 0의 크기에 의해 완전히 결정됩니다.
solution: Experience Manager
title: 합성 캔버스
feature: Dynamic Media Classic,SDK/API
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 0%

---


# 합성 캔버스{#the-compositing-canvas}

req=img인 경우 합성 캔버스의 크기는 레이어 0의 크기에 의해 완전히 결정됩니다.

레이어 0에 대한 `size=`이 명시적으로 지정되지 않은 경우 레이어 변형을 사용하여 합성 캔버스의 크기를 계산합니다(아래 참조).

`req=tmb`인 경우 합성 캔버스의 크기는 레이어 0에 대해 지정된 `size=`에 의해 결정되거나, 크기가 지정되지 않은 경우 합성 캔버스 크기가 보기 레트로 설정됩니다(아래 참조).
