---
title: 이미지 미리 로드
description: 이미지 미리 로드는 init() 메서드를 호출한 직후 로드되고 Viewer SDK 라이브러리, 자산 및 사전 설정 정보가 다운로드되는 동안 표시되는 정적 자산 미리 보기 이미지입니다. 이 사전 로드 이미지의 목적은 뷰어 로드 시간을 시각적으로 향상시키고 컨텐츠를 사용자에게 빠르게 제공하는 것입니다.
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

이미지 미리 로드는 init() 메서드를 호출한 직후 로드되고 Viewer SDK 라이브러리, 자산 및 사전 설정 정보가 다운로드되는 동안 표시되는 정적 자산 미리 보기 이미지입니다. 이 사전 로드 이미지의 목적은 뷰어 로드 시간을 시각적으로 향상시키고 컨텐츠를 사용자에게 빠르게 제공하는 것입니다.

사전 로드 이미지는 무제한 높이를 갖는 응답형 포함 방식인 가장 일반적인 뷰어 포함 방법에 대해 잘 작동합니다. 제한 없는 높이](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435)가 포함된 응답형 디자인 제목을 참조하십시오.[

그러나 이 기능에는 다른 포함 메서드 또는 특정 구성 옵션을 사용할 때 특정 제한 사항이 있습니다. 다음 경우 사전 로드 이미지가 제대로 렌더링되지 않을 수 있습니다.

* 뷰어의 크기가 고정되고 뷰어 사전 설정 레코드 내의 `stagesize` 구성 속성을 사용하여 크기가 정의되는 경우. 또는 최상위 뷰어 컨테이너 요소에 외부 뷰어 CSS 파일을 사용합니다.
* 뷰어 임베딩의 폭 및 높이 정의된 방법과 함께 가요성 크기 임베딩을 사용하는 경우. [너비와 높이가 정의된 유연한 크기 포함 제목](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435)을 참조하십시오.

위에 나열된 작업 모드 중 하나에서 뷰어를 사용하는 경우 `preloadImage` 구성 속성을 사용하여 사전 로드 이미지 기능을 비활성화합니다.

또한, 뷰어가 DOM 요소에 포함된 경우 `display:none` CSS 설정을 사용하여 숨기거나 DOM 트리에서 분리되는 경우 구성에서 활성화되었더라도 사전 로드 이미지가 사용되지 않습니다.
