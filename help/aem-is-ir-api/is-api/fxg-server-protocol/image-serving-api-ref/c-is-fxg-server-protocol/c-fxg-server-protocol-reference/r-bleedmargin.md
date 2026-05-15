---
description: 도련 여백을 설정합니다. PDF 파일에 설정된 도련 여백을 설정합니다.
solution: Experience Manager
title: 재단 여백
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: badb8ca5-52ba-4b44-b53f-fb302626adc4
TQID: 'https://experienceleague.adobe.com/Lghb-4jpksjewoUjBD-SE9UqsD6AX6WFwb2sbkCobXE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 57
ht-degree: 0%

---

# 재단 여백{#bleedmargin}

도련 여백을 설정합니다. PDF 파일에 설정된 도련 여백을 설정합니다.

`bleedMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]`(포인트)

기본적으로 `bleedMargin`은(는) `viewWidth` 및 `viewHeight`에 의해 정의된 문서의 전체 크기로 설정됩니다. 지정하지 않으면 *[!DNL left]*, *[!DNL bottom]* 및 *[!DNL right]* 값이 *[!DNL top]* 값으로 기본 설정됩니다.
