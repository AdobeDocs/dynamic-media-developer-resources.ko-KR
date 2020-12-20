---
description: 일부 응용 프로그램은 다양한 유형의 재질에 대해 다른 조명 맵을 필요로 할 수 있습니다.
seo-description: 일부 응용 프로그램은 다양한 유형의 재질에 대해 다른 조명 맵을 필요로 할 수 있습니다.
seo-title: 여러 조명 맵 사용
solution: Experience Manager
title: 여러 조명 맵 사용
topic: Scene7 Image Serving - Image Rendering API
uuid: 24d86229-6e88-4fe2-80ef-30461aee3db5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---


# 여러 조명 맵 사용{#using-multiple-illumination-maps}

일부 응용 프로그램은 다양한 유형의 재질에 대해 다른 조명 맵을 필요로 할 수 있습니다.

각 비네팅에 대해 최대 3개의 조명 맵을 제작할 수 있습니다. 렌더링 작업에 대한 조명 맵이 `illum=` 및 `gloss=` 명령으로 선택됩니다.

**기본** 선택 `illum=` 과 지정하지 않은 경우 렌더러 `gloss=` 는 첫 번째 제작된 조명 맵(일반적으로 &#39;평면&#39; 조명 맵)을 사용합니다.

**자동 선택`gloss=`** 이 지정되지  `illum=` 않았거나 -1로 설정된 경우 렌더러는 지정된  `gloss=` 값을 비네팅의 각 조명 맵과 연관된 광택 값과 비교하고 광택 값이 지정된 값과 가장 가까운 조명 맵을  `gloss=`선택합니다.

**지정된`illum=`** 경우 0, 1 또 `illum=` 는 2로 설정된 경우 렌더러에서 해당 조명 맵을 사용합니다. `gloss=` 은 조명 맵을 선택할 목적으로 무시됩니다.

비네팅에 조명 맵이 하나만 포함되어 있으면 렌더러는 해당 맵을 사용하고 `illum=` 및 `gloss=` 명령을 무시합니다.
