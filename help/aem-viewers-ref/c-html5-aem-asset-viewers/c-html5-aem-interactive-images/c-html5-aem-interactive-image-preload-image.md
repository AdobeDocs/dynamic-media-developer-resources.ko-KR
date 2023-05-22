---
title: 이미지 미리 로드
description: 미리 로드 이미지는 init() 메서드 호출 직후 로드되고 Viewer SDK 라이브러리, 에셋 및 사전 설정 정보가 다운로드되는 동안 표시되는 정적 에셋 미리 보기 이미지입니다. 프리로드 영상의 목적은 시청자 로드 시간을 시각적으로 개선하고 사용자에게 콘텐츠를 신속하게 제시하는 것이다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 54bea5fc-916c-4a58-bc06-b726884d488a
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# 이미지 미리 로드{#preload-image}

미리 로드 이미지는 init() 메서드 호출 직후 로드되고 Viewer SDK 라이브러리, 에셋 및 사전 설정 정보가 다운로드되는 동안 표시되는 정적 에셋 미리 보기 이미지입니다. 프리로드 영상의 목적은 시청자 로드 시간을 시각적으로 개선하고 사용자에게 콘텐츠를 신속하게 제시하는 것이다.

이미지 미리 로드는 무제한 높이의 반응형 임베딩인 가장 일반적인 뷰어 임베딩 방법에서 적합합니다. 제목 보기 [무제한 높이의 응답형 디자인 임베딩](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

그러나 이 기능은 다른 포함 방법 또는 특정 구성 옵션을 사용할 때 특정 제한 사항이 있습니다. 다음과 같은 경우 이미지 미리 로드가 제대로 렌더링되지 않을 수 있습니다.

* 뷰어의 크기가 고정되어 있고 다음 중 하나를 사용하여 크기가 정의된 경우 `stagesize` 뷰어 사전 설정 레코드 내의 구성 특성입니다. 또는 최상위 뷰어 컨테이너 요소에 외부 뷰어 CSS 파일을 사용합니다.
* 뷰어 임베드의 폭 및 높이 정의된 가변 크기 임베드 사용 시. 제목 보기 [폭 및 높이가 정의된 유연한 크기 포함](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

다음을 사용하여 이미지 미리 로드 기능 비활성화 `preloadImage` 위에 나열된 작업 모드 중 하나에서 뷰어를 사용하는 경우 구성 속성입니다.

또한 뷰어가 DOM 요소에 임베드되어 있는 경우 구성에서 활성화되더라도 프리로드 이미지가 사용되지 않습니다. `display:none` CSS 설정 또는 DOM 트리에서 분리됩니다.
