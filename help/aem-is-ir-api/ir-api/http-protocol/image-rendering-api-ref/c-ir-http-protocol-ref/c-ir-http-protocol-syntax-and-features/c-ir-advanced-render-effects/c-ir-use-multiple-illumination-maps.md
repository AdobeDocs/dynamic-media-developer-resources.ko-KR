---
title: 여러 조명 맵 사용
description: 일부 응용 프로그램들은 다양한 종류의 자료에 대해 다른 조명 맵을 필요로 할 수 있습니다.
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

일부 응용 프로그램들은 다양한 종류의 자료에 대해 다른 조명 맵을 필요로 할 수 있습니다.

각 비네트에 대해 최대 3개의 조명 맵을 작성할 수 있습니다. 렌더링 작업에 대한 조명 맵은 `illum=` 또는 `gloss=` 명령.

**기본 선택** - If `illum=` 또는 `gloss=` 지정하지 않으면 렌더러에서 처음으로 작성된 조명 맵(일반적으로 &#39;플랫&#39; 조명 맵이라고도 함)을 사용합니다.

**자동 선택`gloss=`** - If `illum=` 가 지정되지 않았거나 이 `-1`로 지정하는 렌더러는 지정된 `gloss=` 값 - 비네트의 각 조명 맵과 연관된 광택 값. 광택 값이 지정된 값과 가장 가까운 조명 맵을 선택합니다 `gloss=`.

**을 사용하여 명시적 선택`illum=`** - If `illum=` 가 지정되고 `0`, `1`, 또는 `2`로 지정하는 렌더러는 해당 조명 맵을 사용합니다. `gloss=` 조명 맵을 선택할 때는 이 무시됩니다.

비네트에 조명 맵이 하나만 포함되어 있으면 렌더러는 해당 맵을 사용하고 이 맵을 무시합니다 `illum=` 및 `gloss=` 명령.
