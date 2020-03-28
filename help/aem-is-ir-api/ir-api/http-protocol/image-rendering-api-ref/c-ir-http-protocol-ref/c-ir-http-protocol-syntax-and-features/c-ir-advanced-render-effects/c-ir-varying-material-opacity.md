---
description: 가변 불투명도는 겹쳐진 개체에 적용된 단색 및 반복 텍스처와 도표 및 창 적용 재질에 대해 지원됩니다.
seo-description: 가변 불투명도는 겹쳐진 개체에 적용된 단색 및 반복 텍스처와 도표 및 창 적용 재질에 대해 지원됩니다.
seo-title: 다양한 재료 불투명도
solution: Experience Manager
title: 다양한 재료 불투명도
topic: Scene7 Image Serving - Image Rendering API
uuid: 6af07ea8-44ba-4253-8a26-614725af2f46
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 다양한 재료 불투명도{#varying-material-opacity}

가변 불투명도는 겹쳐진 개체에 적용된 단색 및 반복 텍스처와 도표 및 창 적용 재질에 대해 지원됩니다.

알파 채널과 함께 RGB 이미지를 사용하면 불투명도 정보를 간단하게 제공할 수 있습니다. 또한 RGB 및 RGBA 이미지의 경우 `opacity=` 명령을 사용하여 전체 불투명도를 변경할 수 있습니다.

벽 테두리는 RGBA 이미지를 지원하며 주로 다이 컷 테두리를 지원합니다.

창 커버링을 정의하는 [!DNL vnw] 파일에는 불투명도 채널이 포함될 수 있습니다. 이 채널은 렌더러에 의해 반복 가능한 텍스처의 알파 채널과 `opacity=` 값을 결합하여 완전한 투명도 및 반투명 창 처리를 위한 다양한 불투명도 효과를 제공합니다.
