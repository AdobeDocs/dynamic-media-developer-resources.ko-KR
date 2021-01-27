---
description: 뷰어는 Dynamic Media Classic 또는 AEM Dynamic Media 외부에 호스팅된 비디오 재생을 지원합니다.
solution: Experience Manager
title: 외부 비디오 지원
topic: Dynamic Media
translation-type: tm+mt
source-git-commit: dacd641302826196f4bf4c8d2dfc02d032d63487
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---


# 외부 비디오 지원{#external-video-support}

뷰어는 Dynamic Media Classic 또는 AEM Dynamic Media 외부에 호스팅된 비디오 재생을 지원합니다.

외부 비디오에 대해 지원되는 형식은 H.264 형식의 MP4 또는 HLS 스트림에 대한 M3U8 매니페스트입니다.

뷰어는 Dynamic Media Classic 또는 AEM Dynamic Media 비디오나 외부 비디오에서 사용할 수 있습니다. 뷰어가 Dynamic Media Classic/Dynamic Media 비디오으로 시작하는 경우 앞으로 나가는 에셋 형식과 함께 사용하면 [ `setVideo`](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) 메서드를 사용하여 외부 비디오를 이 뷰어로 로드할 수 없습니다. 비구절.뷰어가 처음에 외부 비디오와 함께 로드된 경우 외부 비디오만 사용하여 작업해야 합니다.

외부 비디오를 사용하여 작업할 때 뷰어는 재생 수정자의 값을 무시하고 외부 비디오 확장자에서 재생 유형을 감지합니다. 외부 비디오 URL이 .m3u8로 끝나는 경우 뷰어에서 HLS 재생을 사용하는 경우 점진적 재생이 사용됩니다.
