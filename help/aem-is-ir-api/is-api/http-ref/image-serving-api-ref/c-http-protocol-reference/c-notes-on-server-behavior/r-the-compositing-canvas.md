---
description: req=img이면 합성 캔버스의 크기는 레이어 0의 크기에 의해 완전히 결정됩니다.
solution: Experience Manager
title: 합성 캔버스
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 38b2349f-714a-4304-bd33-5ce171b6d3a1
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 0%

---

# 합성 캔버스{#the-compositing-canvas}

req=img이면 합성 캔버스의 크기는 레이어 0의 크기에 의해 완전히 결정됩니다.

레이어 0에 대한 `size=` 을 명시적으로 지정하지 않으면 레이어 변형을 사용하여 합성 캔버스의 크기를 계산합니다(아래 참조).

`req=tmb` 이면 합성 캔버스의 크기가 레이어 0에 대해 지정된 `size=`에 의해 결정되거나, 크기를 지정하지 않으면 합성 캔버스 크기가 보기 레코드로 설정됩니다(아래 참조).
