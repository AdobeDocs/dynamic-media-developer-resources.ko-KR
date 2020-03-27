---
description: 일부 제한 사항은 중첩과 임베드할 때 적용됩니다.
seo-description: 일부 제한 사항은 중첩과 임베드할 때 적용됩니다.
seo-title: 제한 사항
solution: Experience Manager
title: 제한 사항
topic: Scene7 Image Serving - Image Rendering API
uuid: 05e97255-db4d-4587-94d2-a7ea608ff7d4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Restrictions{#restrictions}

일부 제한 사항은 중첩과 임베드할 때 적용됩니다.

서버 성능을 향상시키기 위해 중첩된 요청으로 반환되는 이미지의 해상도는 자료가 적용되는 객체의 텍스처 해상도와 합리적으로 일치해야 합니다.

외부 이미지는 로컬에 캐시됩니다. 이러한 이미지에 대한 모든 변경 사항은 로컬 캐시 항목이 오래된(만료 HTTP 헤더를 기반으로) 후에만 감지됩니다.
