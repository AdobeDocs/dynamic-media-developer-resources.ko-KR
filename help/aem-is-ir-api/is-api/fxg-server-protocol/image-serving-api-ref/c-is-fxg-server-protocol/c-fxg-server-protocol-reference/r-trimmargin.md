---
description: 트리밍 여백을 설정합니다. PDF 파일에 설정된 트림 여백을 설정합니다.
solution: Experience Manager
title: trimMargin
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dc6e31f8-d3be-44d3-8342-a4ef4b3fd61b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 0%

---

# trimMargin{#trimmargin}

트리밍 여백을 설정합니다. PDF 파일에 설정된 트림 여백을 설정합니다.

` trimMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]`(포인트)

기본적으로 `trimMargin`은(는) `viewWidth` 및 `viewHeight`에 의해 정의된 문서의 전체 크기로 설정됩니다. 지정하지 않으면 *[!DNL left]*, *[!DNL bottom]* 및 *[!DNL right]* 값이 *[!DNL top]* 값으로 기본 설정됩니다.
