---
description: 겹치는 오브젝트에 적용된 단색 및 반복 가능한 텍스쳐뿐만 아니라, 전사 및 창 덮는 재료에도 가변 불투명도가 지원됩니다.
solution: Experience Manager
title: 다양한 재료 불투명도
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 65f4b578-0c64-4515-8184-2908b317a983
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# 다양한 재료 불투명도{#varying-material-opacity}

겹치는 오브젝트에 적용된 단색 및 반복 가능한 텍스쳐뿐만 아니라, 전사 및 창 덮는 재료에도 가변 불투명도가 지원됩니다.

알파 채널과 함께 RGB 영상을 이용하여 불투명도 정보를 간단히 제공할 수 있다. 또한 전체 불투명도는 `opacity=` 명령(RGB 및 RGBA 이미지의 경우 모두)으로 변경될 수 있습니다.

벽면 테두리도 RGBA 이미지를 지원하며 주로 금형 테두리를 지원합니다.

윈도우 커버링을 정의하는 [!DNL vnw] 파일에는 렌더러에 의해 반복 가능한 텍스처의 알파 채널과 `opacity=` 값이 결합된 불투명도 채널이 포함되어 완전 및 반투명 창 처리를 위한 다양한 불투명도 효과를 제공할 수 있습니다.
