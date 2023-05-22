---
title: 제한 사항
description: 일부 제한 사항은 중첩 및 포함에 적용됩니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac2fd40b-a2f6-4f6f-9d10-3da3d701042b
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 0%

---

# 제한 사항{#restrictions}

일부 제한 사항은 중첩 및 포함에 적용됩니다.

서버 성능이 좋으려면 중첩 요청에서 반환된 이미지의 해상도가 재료가 적용되는 객체의 텍스처 해상도와 합리적으로 일치해야 합니다.

외부 이미지가 로컬에서 캐시됩니다. 이러한 이미지에 대한 모든 변경 사항은 로컬 캐시 항목이 오래된 경우에만 감지됩니다(만료 HTTP 헤더 기반).
