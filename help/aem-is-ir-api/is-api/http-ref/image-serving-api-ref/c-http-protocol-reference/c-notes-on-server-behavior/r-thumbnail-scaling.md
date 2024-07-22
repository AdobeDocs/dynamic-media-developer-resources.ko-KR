---
title: 썸네일 크기 조정
description: 이미지 레이어 변환의 2단계는 썸네일(즉, req=tmb)에 대해 다음과 같이 수정됩니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08290258-4fc8-4a6a-ba8f-6bdcd969fa3c
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 0%

---

# 썸네일 크기 조정{#thumbnail-scaling}

이미지 레이어 변환의 2단계는 썸네일(즉, req=tmb)에 대해 다음과 같이 수정됩니다.

* `2.` `size=`이(가) 지정된 경우 썸네일 규칙을 사용하여 (잘린) 이미지를 `size=` rect에 맞춥니다. `size=`을(를) 지정하지 않은 경우 `res=`을(를) 기준으로 크기를 조정하거나 `res=`을(를) 지정하지 않은 경우 아래 요약된 썸네일 규칙을 사용하여 (잘린) 이미지를 캔버스 rect에 맞춥니다.
