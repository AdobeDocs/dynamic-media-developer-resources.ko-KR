---
description: 대부분의 재료는 동적으로 색상화할 수 있습니다.
seo-description: 대부분의 재료는 동적으로 색상화할 수 있습니다.
seo-title: 재질 색상화
solution: Experience Manager
title: 재질 색상화
uuid: 3f5a9089-6e35-446c-89f9-71b067e0d1df
feature: Dynamic Media Classic,SDK/API
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---


# 재질 색상화{#colorizing-materials}

대부분의 재료는 동적으로 색상화할 수 있습니다.

색상화 알고리즘은 매우 간단하며 색조 범위가 제한된 재료 이미지에 가장 적합합니다. 재질을 색상화하려면 렌더러는 `bgc=` 값을 빼고 각 픽셀 값에 `color=` 값을 추가합니다.

`color=`이(가) 지정되지 않은 경우 색상화가 비활성화됩니다. `bgc=` 는 캐비닛 자료에 의해 무시됩니다.파일에 포함된 기본 색상 값이  [!DNL vnc] 대신 사용됩니다.
