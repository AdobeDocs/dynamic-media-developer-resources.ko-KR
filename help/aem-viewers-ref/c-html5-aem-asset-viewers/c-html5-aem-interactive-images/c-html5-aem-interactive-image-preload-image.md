---
description: 미리 로드 이미지는 init() 메서드를 호출한 후 바로 로드되고 Viewer SDK 라이브러리, 자산 및 사전 설정 정보가 다운로드되는 동안 표시되는 정적 자산 미리 보기 이미지입니다. 미리 로드 이미지의 목적은 뷰어 로드 시간을 시각적으로 향상시키고 컨텐츠를 사용자에게 신속하게 제공하는 것입니다.
seo-description: 미리 로드 이미지는 init() 메서드를 호출한 후 바로 로드되고 Viewer SDK 라이브러리, 자산 및 사전 설정 정보가 다운로드되는 동안 표시되는 정적 자산 미리 보기 이미지입니다. 미리 로드 이미지의 목적은 뷰어 로드 시간을 시각적으로 향상시키고 컨텐츠를 사용자에게 신속하게 제공하는 것입니다.
seo-title: 이미지 미리 로드
solution: Experience Manager
title: 이미지 미리 로드
topic: Dynamic media
uuid: cb5db16d-b496-40e4-b8ef-5573c42d2850
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 이미지 미리 로드{#preload-image}

미리 로드 이미지는 init() 메서드를 호출한 후 바로 로드되고 Viewer SDK 라이브러리, 자산 및 사전 설정 정보가 다운로드되는 동안 표시되는 정적 자산 미리 보기 이미지입니다. 미리 로드 이미지의 목적은 뷰어 로드 시간을 시각적으로 향상시키고 컨텐츠를 사용자에게 신속하게 제공하는 것입니다.

미리 로드 이미지는 무제한 높이로 임베드하는 응답형 뷰어 임베드 방식에 적합합니다. 제한 없는 높이로 [포함된 반응형 디자인](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435)제목을 참조하십시오.

그러나 다른 포함 방법 또는 특정 구성 옵션이 사용될 경우 이 기능에는 특정 제한이 있습니다. 다음 경우 미리 로드 이미지가 제대로 렌더링되지 않을 수 있습니다.

* 뷰어의 크기가 수정되고 크기가 뷰어 사전 설정 레코드 내의 구성 속성을 사용하여 정의되거나 최상위 뷰어 컨테이너 요소에 대한 외부 뷰어 CSS 파일에 정의됩니다. `stagesize`
* 뷰어 임베딩의 정의된 폭 및 높이와 함께 유연한 크기 임베딩을 사용하는 경우 너비 및 [높이가 정의된](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435)유연한 크기 임베드 머리글을 참조하십시오.

위에 나열된 작업 모드 중 하나에서 뷰어를 사용하는 경우 구성 속성을 사용하여 미리 로드 이미지 기능을 비활성화해야 할 수 있습니다. `preloadImage`

또한, 미리 로드 이미지는 구성에서 활성화된 경우에도 사용되지 않습니다. 뷰어가 CSS 설정을 사용하여 DOM 요소에 `display:none` 포함되거나 DOM 트리에서 분리되는 경우 이 구성 요소에 포함됩니다.
