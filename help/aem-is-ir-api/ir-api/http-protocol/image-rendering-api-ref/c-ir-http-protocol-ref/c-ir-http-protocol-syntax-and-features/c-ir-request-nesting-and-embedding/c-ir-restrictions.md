---
description: 일부 제한 사항은 중첩 및 포함에 적용됩니다.
solution: Experience Manager
title: 제한 사항
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac2fd40b-a2f6-4f6f-9d10-3da3d701042b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 0%

---

# 제한 사항{#restrictions}

일부 제한 사항은 중첩 및 포함에 적용됩니다.

서버 성능이 좋은 경우, 중첩된 요청으로 반환되는 이미지의 해상도는 재료가 적용되는 개체의 텍스처 해상도와 합리적으로 일치해야 합니다.

외부 이미지는 로컬로 캐시됩니다. 이러한 이미지에 대한 모든 변경 사항은 로컬 캐시 항목이 오래된(만료된 HTTP 헤더를 기반으로) 후에만 감지됩니다.
