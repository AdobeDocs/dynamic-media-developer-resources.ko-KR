---
title: 재료 색상화
description: 대부분의 재료는 동적으로 색칠될 수 있습니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 95b13a57-f10b-4ff2-90fd-507e69cb2b04
TQID: 'https://experienceleague.adobe.com/MGmuOj214tFPKeSGwz33pGn2m0B0fme1Cq-umlxG9v0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 76
ht-degree: 0%

---

# 재료 색상화{#colorizing-materials}

대부분의 재료는 동적으로 색칠될 수 있습니다.

색상화 알고리즘은 단순하며 색조 범위가 제한된 재료 이미지에 가장 적합합니다. 재료를 색상화하기 위해 렌더러는 `bgc=` 값을 빼고 각 픽셀 값에 `color=` 값을 추가하기만 하면 됩니다.

`color=`이(가) 지정되지 않은 경우 색상화가 비활성화됩니다. 캐비닛 자재에서는 `bgc=` 특성을 무시합니다. 대신 [!DNL vnc] 파일에 포함된 기본 색상 값이 사용됩니다.
