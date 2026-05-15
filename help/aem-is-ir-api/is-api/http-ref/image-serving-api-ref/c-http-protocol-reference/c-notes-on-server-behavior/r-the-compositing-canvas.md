---
description: req=img인 경우, 합성 캔버스의 크기는 전적으로 레이어 0의 크기에 의해 결정된다.
solution: Experience Manager
title: 합성 캔버스
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 38b2349f-714a-4304-bd33-5ce171b6d3a1
TQID: 'https://experienceleague.adobe.com/62uvC05pApoYR5lY4A-KA5RHmW8Xz0r2-2yvOpdAkOo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 99
ht-degree: 0%

---

# 합성 캔버스{#the-compositing-canvas}

req=img인 경우, 합성 캔버스의 크기는 전적으로 레이어 0의 크기에 의해 결정된다.

레이어 0에 대한 `size=`이(가) 명시적으로 지정되지 않은 경우 레이어 변형을 사용하여 합성 캔버스의 크기를 계산합니다(아래 참조).

`req=tmb`의 경우 레이어 0에 대해 지정된 `size=`에 의해 합성 캔버스의 크기가 결정되거나, 크기가 지정되지 않은 경우 합성 캔버스 크기가 뷰 rect로 설정됩니다(아래 참조).
