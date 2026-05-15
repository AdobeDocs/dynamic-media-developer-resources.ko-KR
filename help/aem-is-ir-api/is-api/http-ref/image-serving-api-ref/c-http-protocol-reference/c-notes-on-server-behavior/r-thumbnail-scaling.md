---
title: 썸네일 크기 조정
description: 이미지 레이어 변환의 2단계는 썸네일(즉, req=tmb)에 대해 다음과 같이 수정됩니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08290258-4fc8-4a6a-ba8f-6bdcd969fa3c
TQID: 'https://experienceleague.adobe.com/He10BtjrEIOQW6SZcaUhcExDjP05BR-pc3BCj9TRawU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 79
ht-degree: 0%

---

# 썸네일 크기 조정{#thumbnail-scaling}

이미지 레이어 변환의 2단계는 썸네일(즉, req=tmb)에 대해 다음과 같이 수정됩니다.

* `2.` `size=`이(가) 지정된 경우 썸네일 규칙을 사용하여 (잘린) 이미지를 `size=` rect에 맞춥니다. `size=`을(를) 지정하지 않은 경우 `res=`을(를) 기준으로 크기를 조정하거나 `res=`을(를) 지정하지 않은 경우 아래 요약된 썸네일 규칙을 사용하여 (잘린) 이미지를 캔버스 rect에 맞춥니다.
