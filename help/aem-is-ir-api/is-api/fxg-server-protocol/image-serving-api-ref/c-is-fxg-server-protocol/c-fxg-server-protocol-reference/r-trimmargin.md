---
description: 트림 여백을 설정합니다. PDF 파일에 설정된 트림 여백을 설정합니다.
solution: Experience Manager
title: trimMargin
feature: Dynamic Media Classic,SDK/API
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 0%

---


# trimMargin{#trimmargin}

트림 여백을 설정합니다. PDF 파일에 설정된 트림 여백을 설정합니다.

` trimMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` 포인트

기본적으로 `trimMargin`은 `viewWidth` 및 `viewHeight`에서 정의한 문서의 전체 크기로 설정됩니다. *[!DNL left]*, *[!DNL bottom]* 및 *[!DNL right]* 값은 지정되지 않은 경우 기본적으로 *[!DNL top]* 값으로 설정됩니다.
