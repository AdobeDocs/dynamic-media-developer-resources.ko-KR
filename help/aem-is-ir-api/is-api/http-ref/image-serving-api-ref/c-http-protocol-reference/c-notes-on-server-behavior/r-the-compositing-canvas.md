---
description: req=img인 경우, 합성 캔버스의 크기는 전적으로 레이어 0의 크기에 의해 결정된다.
solution: Experience Manager
title: 합성 캔버스
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 38b2349f-714a-4304-bd33-5ce171b6d3a1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 0%

---

# 합성 캔버스{#the-compositing-canvas}

req=img인 경우, 합성 캔버스의 크기는 전적으로 레이어 0의 크기에 의해 결정된다.

레이어 0에 대한 `size=`이(가) 명시적으로 지정되지 않은 경우 레이어 변형을 사용하여 합성 캔버스의 크기를 계산합니다(아래 참조).

`req=tmb`의 경우 레이어 0에 대해 지정된 `size=`에 의해 합성 캔버스의 크기가 결정되거나, 크기가 지정되지 않은 경우 합성 캔버스 크기가 뷰 rect로 설정됩니다(아래 참조).
