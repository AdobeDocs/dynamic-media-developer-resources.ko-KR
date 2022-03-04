---
title: 색소 소재
description: 대부분의 재료들은 동적으로 색화할 수 있다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 95b13a57-f10b-4ff2-90fd-507e69cb2b04
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 0%

---

# 색소 소재{#colorizing-materials}

대부분의 재료들은 동적으로 색화할 수 있다.

색상화 알고리즘은 단순화되며 제한된 색상 범위를 갖는 재료 이미지에 가장 적합합니다. 재료의 색상을 조정하려면 렌더러는 단순히 `bgc=` 값과 추가 `color=` 값을 각 픽셀 값에 지정합니다.

Colorization은 `color=` 이 지정되지 않았습니다. 다음 `bgc=` 속성은 캐비닛 자료에 의해 무시됩니다. 에 포함된 기본 색상 값 [!DNL vnc] 파일이 대신 사용됩니다.
