---
title: 여러 조명 맵 사용
description: 일부 애플리케이션들은 상이한 종류의 재료들에 대해 상이한 조명 맵을 요구할 수 있다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a6e0be23-8b8a-4b60-aac1-c692319a0bce
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---

# 여러 조명 맵 사용{#using-multiple-illumination-maps}

일부 애플리케이션들은 상이한 종류의 재료들에 대해 상이한 조명 맵을 요구할 수 있다.

비네팅 각각에 대해 최대 3개의 조명 맵을 작성할 수 있습니다. 렌더링 작업에 대한 조명 맵이 `illum=` 및 또는 `gloss=` 명령입니다.

**기본 선택** - 경우 `illum=` 또는 `gloss=` 가 지정되지 않은 경우 렌더러는 첫 번째로 작성된 조명 맵(일반적으로 맵 A, 일명 &#39;플랫&#39; 조명 맵)을 사용합니다.

**다음을 포함한 자동 선택`gloss=`** - 경우 `illum=` 이(가) 지정되지 않았거나 가 (으)로 설정된 경우 `-1`, 렌더러는 지정된 을 비교합니다. `gloss=` 비네팅의 각 조명 맵과 연관된 광택 값이 포함된 값입니다. 광택 값이 지정된 값에 가장 가까운 조명 맵을 선택합니다 `gloss=`.

**다음을 포함한 명시적 선택`illum=`** - 경우 `illum=` 이(가) 지정되고 이(가) (으)로 설정됩니다. `0`, `1`, 또는 `2`, 렌더러는 해당 조명 맵을 사용합니다. `gloss=` 조명 맵을 선택할 때는 가 무시됩니다.

비네팅에 조명 맵이 하나만 포함되어 있으면 렌더러는 해당 맵을 사용하고 를 무시합니다 `illum=` 및 `gloss=` 명령입니다.
