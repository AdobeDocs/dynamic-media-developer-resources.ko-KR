---
description: 가변 불투명도는 겹쳐진 오브젝트뿐만 아니라 디캘과 윈도 덮는 재질에 적용되는 단색 및 반복 가능한 텍스처에 지원됩니다.
seo-description: 가변 불투명도는 겹쳐진 오브젝트뿐만 아니라 디캘과 윈도 덮는 재질에 적용되는 단색 및 반복 가능한 텍스처에 지원됩니다.
seo-title: 다양한 재질 불투명도
solution: Experience Manager
title: 다양한 재질 불투명도
topic: Scene7 Image Serving - Image Rendering API
uuid: 6af07ea8-44ba-4253-8a26-614725af2f46
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---


# 다양한 재료 불투명도{#varying-material-opacity}

가변 불투명도는 겹쳐진 오브젝트뿐만 아니라 디캘과 윈도 덮는 재질에 적용되는 단색 및 반복 가능한 텍스처에 지원됩니다.

알파 채널이 있는 RGB 이미지를 사용하여 불투명도 정보를 간단히 제공할 수 있습니다. 또한 전체 불투명도는 `opacity=` 명령(RGB 및 RGBA 이미지의 경우 모두)으로 변경할 수 있습니다.

벽 테두리도 RGBA 이미지를 지원하며 주로 다이 컷 테두리를 지원합니다.

윈도우 커버를 정의하는 [!DNL vnw] 파일에는 불투명도 채널이 포함될 수 있습니다. 이 채널은 반복 가능한 텍스처의 알파 채널 및 `opacity=` 값과 렌더러에 의해 결합되어 완전 및 반투명 윈도우 처리를 위한 다양한 불투명도 효과를 제공합니다.
