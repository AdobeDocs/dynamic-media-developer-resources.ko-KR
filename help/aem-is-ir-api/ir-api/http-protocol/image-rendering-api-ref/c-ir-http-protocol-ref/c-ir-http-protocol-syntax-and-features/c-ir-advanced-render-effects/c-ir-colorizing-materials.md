---
description: 대부분의 재료들은 동적으로 색화할 수 있다.
solution: Experience Manager
title: 색소 소재
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 95b13a57-f10b-4ff2-90fd-507e69cb2b04
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---

# 색소 소재{#colorizing-materials}

대부분의 재료들은 동적으로 색화할 수 있다.

색상화 알고리즘은 매우 단순하며 제한된 색상 범위를 갖는 재료 이미지에 가장 적합합니다. 물질의 색상을 조정하려면 렌더러는 `bgc=` 값을 빼고 각 픽셀 값에 `color=` 값을 추가합니다.

`color=` 이 지정되지 않은 경우 색조가 비활성화됩니다. `bgc=` 는 캐비닛 자료에 의해 무시됩니다. 파일에 포함된 기본 색상  [!DNL vnc] 값이 대신 사용됩니다.
