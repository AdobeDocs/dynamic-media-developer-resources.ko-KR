---
description: 도련 여백을 설정합니다. PDF 파일에 설정된 도련 여백을 설정합니다.
solution: Experience Manager
title: 재단 여백
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: badb8ca5-52ba-4b44-b53f-fb302626adc4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 0%

---

# 재단 여백{#bleedmargin}

도련 여백을 설정합니다. PDF 파일에 설정된 도련 여백을 설정합니다.

`bleedMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]`(포인트)

기본적으로 `bleedMargin`은(는) `viewWidth` 및 `viewHeight`에 의해 정의된 문서의 전체 크기로 설정됩니다. 지정하지 않으면 *[!DNL left]*, *[!DNL bottom]* 및 *[!DNL right]* 값이 *[!DNL top]* 값으로 기본 설정됩니다.
