---
description: 대부분의 재료는 동적으로 색상을 적용할 수 있습니다.
seo-description: 대부분의 재료는 동적으로 색상을 적용할 수 있습니다.
seo-title: 재질 색상화
solution: Experience Manager
title: 재질 색상화
topic: Scene7 Image Serving - Image Rendering API
uuid: 3f5a9089-6e35-446c-89f9-71b067e0d1df
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 재질 색상화{#colorizing-materials}

대부분의 재료는 동적으로 색상을 적용할 수 있습니다.

색상화 알고리즘은 매우 간단하며 색조 범위가 제한된 재료 이미지에 가장 적합합니다. 재질을 색상화하기 위해 렌더러는 값을 빼고 각 픽셀 값에 `bgc=` `color=` 값을 추가합니다.

색상을 지정하지 않으면 `color=` 색상화가 비활성화됩니다. `bgc=` 는 캐비닛 자료에 의해 무시됩니다.파일에 포함된 기본 색상 값이 대신 사용됩니다. [!DNL vnc]
