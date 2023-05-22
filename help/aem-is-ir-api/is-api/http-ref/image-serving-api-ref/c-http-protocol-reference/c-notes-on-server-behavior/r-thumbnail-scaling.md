---
description: 이미지 레이어 변환의 2단계는 썸네일에 대해 다음과 같이 수정됩니다(즉, req=tmb인 경우).
solution: Experience Manager
title: 썸네일 크기 조정
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08290258-4fc8-4a6a-ba8f-6bdcd969fa3c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 0%

---

# 썸네일 크기 조정{#thumbnail-scaling}

이미지 레이어 변환의 2단계는 썸네일에 대해 다음과 같이 수정됩니다(즉, req=tmb인 경우).

* `2.` If `size=` 이(가) 지정되어 있으면 (자른) 이미지를 `size=` 썸네일 규칙을 사용하여 rect합니다. If `size=` 이(가) 지정되지 않았습니다. 다음을 기준으로 크기 조절 `res=`, 또는, `res=` 을 지정하지 않은 경우 아래에 요약된 썸네일 규칙을 사용하여 (잘린) 이미지를 캔버스 rect에 맞춥니다.
