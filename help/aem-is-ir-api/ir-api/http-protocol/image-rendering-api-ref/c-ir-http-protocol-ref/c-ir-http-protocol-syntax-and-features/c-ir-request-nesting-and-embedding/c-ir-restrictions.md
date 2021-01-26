---
description: 일부 제한 사항은 중첩 및 포함에 적용됩니다.
seo-description: 일부 제한 사항은 중첩 및 포함에 적용됩니다.
seo-title: 제한 사항
solution: Experience Manager
title: 제한 사항
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 05e97255-db4d-4587-94d2-a7ea608ff7d4
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---


# 제한 사항{#restrictions}

일부 제한 사항은 중첩 및 포함에 적용됩니다.

서버 성능을 좋게 하기 위해 중첩된 요청에 의해 반환되는 이미지의 해상도는 해당 자료가 적용되는 객체의 텍스처 해상도와 합리적으로 일치해야 합니다.

외부 이미지는 로컬에 캐시됩니다. 이러한 이미지에 대한 모든 변경 사항은 로컬 캐시 항목이 부실(만료 HTTP 헤더를 기반으로 함)된 후에만 감지됩니다.
