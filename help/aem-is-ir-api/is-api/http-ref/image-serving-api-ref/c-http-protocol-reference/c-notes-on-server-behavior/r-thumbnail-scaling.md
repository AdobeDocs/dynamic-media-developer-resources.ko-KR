---
description: '이미지 레이어 변형 2단계는 축소판 그림(예: req=tmb인 경우)에 대해 다음과 같이 수정됩니다.'
solution: Experience Manager
title: 축소판 크기 조절
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08290258-4fc8-4a6a-ba8f-6bdcd969fa3c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---

# 축소판 크기 조절{#thumbnail-scaling}

이미지 레이어 변형 2단계는 축소판 그림(예: req=tmb인 경우)에 대해 다음과 같이 수정됩니다.

* `2.` 이  `size=` 지정된 경우 축소판 규칙을 사용하여 (잘린) 이미지 `size=` 를 최신 이미지에 맞춥니다. `size=`을 지정하지 않은 경우 `res=`을 기준으로 크기를 조정하거나 `res=`를 지정하지 않은 경우 아래 요약된 축소판 규칙을 사용하여 캔버스 필터에 이미지를 맞추십시오.
