---
title: 이미지 미리 로드
description: 미리 로드 이미지는 init() 메서드 호출 직후 로드되고 Viewer SDK 라이브러리, 에셋 및 사전 설정 정보가 다운로드되는 동안 표시되는 정적 에셋 미리 보기 이미지입니다. 프리로드 영상의 목적은 시청자 로드 시간을 시각적으로 개선하고 사용자에게 콘텐츠를 신속하게 제시하는 것이다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 8caf156f-d641-44e9-94f9-5ba3245061a3
source-git-commit: 4aaa77b1fb58b30b02ee15f6080169fa354d5907
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# 이미지 미리 로드{#preload-image}

미리 로드 이미지는 init() 메서드 호출 직후 로드되고 Viewer SDK 라이브러리, 에셋 및 사전 설정 정보가 다운로드되는 동안 표시되는 정적 에셋 미리 보기 이미지입니다. 프리로드 영상의 목적은 시청자 로드 시간을 시각적으로 개선하고 사용자에게 콘텐츠를 신속하게 제시하는 것이다.

이미지 미리 로드는 무제한 높이의 반응형 임베딩인 가장 일반적인 뷰어 임베딩 방법에서 적합합니다. 제목 [무제한 높이의 응답형 디자인 포함](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel.md#concept-b44f1df3c1c64d4e8b5565e7736bf95e)을 참조하세요.

그러나 이 기능은 다른 포함 방법 또는 특정 구성 옵션을 사용할 때 특정 제한 사항이 있습니다. 다음과 같은 경우 이미지 미리 로드가 제대로 렌더링되지 않을 수 있습니다.

* 뷰어의 크기가 고정되어 있고 크기가 뷰어 사전 설정 레코드 내의 `stagesize` 구성 특성을 사용하거나 최상위 뷰어 컨테이너 요소의 외부 뷰어 CSS 파일에서 정의된 경우.
* 뷰어 임베드의 폭 및 높이 정의된 가변 크기 임베드 사용 시. [너비와 높이가 정의된 유연한 크기 포함](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435) 제목을 참조하십시오.

위에 나열된 작업 모드 중 하나에서 뷰어를 사용하는 경우 `preloadImage` 구성 특성을 사용하여 이미지 미리 로드 기능을 비활성화합니다.

또한 뷰어가 `display:none` CSS 설정을 사용하여 숨겨져 있거나 DOM 트리에서 분리된 경우 구성에서 활성화된 경우에도 미리 로드된 이미지가 사용되지 않습니다.
