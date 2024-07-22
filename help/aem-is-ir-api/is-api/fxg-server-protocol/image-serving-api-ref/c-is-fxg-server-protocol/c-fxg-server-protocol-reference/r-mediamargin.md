---
description: 미디어 여백을 설정합니다. PDF 파일에 설정된 미디어 여백을 설정합니다.
solution: Experience Manager
title: mediaMargin
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5bba0dc2-a496-4380-9def-12f9e683eafb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 0%

---

# mediaMargin{#mediamargin}

미디어 여백을 설정합니다. PDF 파일에 설정된 미디어 여백을 설정합니다.

` mediaMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]`(포인트)

기본적으로 `mediaMargin`은(는) `viewWidth` 및 `viewHeight`에 의해 정의된 문서의 전체 크기로 설정됩니다. 지정하지 않으면 *[!DNL left]*, *[!DNL bottom]* 및 *[!DNL right]* 값이 *[!DNL top]* 값으로 기본 설정됩니다.
