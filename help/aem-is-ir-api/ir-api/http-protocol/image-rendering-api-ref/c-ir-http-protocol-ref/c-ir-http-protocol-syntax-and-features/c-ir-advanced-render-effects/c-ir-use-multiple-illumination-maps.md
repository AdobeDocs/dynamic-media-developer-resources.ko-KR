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

비네팅 각각에 대해 최대 3개의 조명 맵을 작성할 수 있습니다. 렌더링 작업에 대한 조명 맵이 `illum=` 및 `gloss=` 명령으로 선택됩니다.

**기본 선택** - `illum=` 또는 `gloss=`을(를) 지정하지 않으면 렌더러가 처음 작성된 조명 맵(일반적으로 맵 A, 일명 &#39;플랫&#39; 조명 맵)을 사용합니다.

**을(를) 사용한`gloss=`**&#x200B;자동 선택 - `illum=`이(가) 지정되지 않았거나 `-1`(으)로 설정된 경우 렌더러는 지정된 `gloss=` 값을 비네팅의 각 조명 맵과 연결된 광택 값과 비교합니다. 광택 값이 지정된 `gloss=`에 가장 가까운 조명 맵을 선택합니다.

**을(를) 사용한`illum=`**&#x200B;명시적 선택 - `illum=`이(가) 지정되어 있고 `0`, `1` 또는 `2`(으)로 설정된 경우 렌더러가 해당 조명 맵을 사용합니다. `gloss=`은(는) 조명 맵을 선택할 때 무시됩니다.

비네팅에 조명 맵이 하나만 포함되어 있으면 렌더러는 해당 맵을 사용하고 `illum=` 및 `gloss=` 명령을 무시합니다.
