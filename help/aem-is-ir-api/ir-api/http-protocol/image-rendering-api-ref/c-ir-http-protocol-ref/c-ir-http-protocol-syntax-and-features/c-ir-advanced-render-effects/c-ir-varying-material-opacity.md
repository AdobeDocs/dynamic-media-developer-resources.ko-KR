---
title: 다양한 재질 불투명도
description: 겹쳐진 오브젝트에 적용된 단색 및 반복 가능한 텍스쳐와 데칼 및 창 커버링 재료에 대해 가변 불투명도가 지원됩니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 65f4b578-0c64-4515-8184-2908b317a983
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# 다양한 재질 불투명도{#varying-material-opacity}

겹쳐진 오브젝트에 적용된 단색 및 반복 가능한 텍스쳐와 데칼 및 창 커버링 재료에 대해 가변 불투명도가 지원됩니다.

불투명도 정보는 알파 채널이 있는 RGB 이미지를 사용함으로써 간단하게 제공할 수 있습니다. 또한 `opacity=` 명령(RGB 및 RGBA 이미지 모두)을 사용하여 전체 불투명도를 변경할 수 있습니다.

벽 경계는 주로 다이 컷 경계를 지원하기 위해 RGBA 이미지를 지원합니다.

창 변환을 정의하는 [!DNL vnw] 파일에 불투명도 채널이 포함될 수 있습니다. 렌더러에서 반복 가능한 텍스처의 알파 채널과 `opacity=` 값을 사용하여 결합되어 투명 및 반투명 창 처리에 대한 전체 범위의 불투명도 효과를 제공합니다.
