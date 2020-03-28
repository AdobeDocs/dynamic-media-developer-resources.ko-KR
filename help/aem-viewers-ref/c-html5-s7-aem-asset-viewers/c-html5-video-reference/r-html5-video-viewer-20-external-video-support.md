---
description: 뷰어는 Scene7 Publishing System 또는 AEM Dynamic Media 외부에서 호스팅된 비디오 재생을 지원합니다.
seo-description: 뷰어는 Scene7 Publishing System 또는 AEM Dynamic Media 외부에서 호스팅된 비디오 재생을 지원합니다.
seo-title: 외부 비디오 지원
solution: Experience Manager
title: 외부 비디오 지원
topic: Dynamic media
uuid: 24739a5a-3a5d-49b8-9a15-bcf3a95fc192
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 외부 비디오 지원{#external-video-support}

뷰어는 Scene7 Publishing System 또는 AEM Dynamic Media 외부에서 호스팅된 비디오 재생을 지원합니다.

외부 비디오에 지원되는 형식은 H.264 형식의 MP4 또는 HLS 스트림에 대한 M3U8 매니페스트입니다.

뷰어는 Scene7 또는 Dynamic Media 비디오 또는 외부 비디오에서 작동할 수 있습니다. 뷰어가 Scene7/Dynamic Media 비디오로 시작하는 경우, 그런 자산 유형이 앞으로 진행되면 [ `setVideo`](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) 방법을 사용하여 외부 비디오를 이 뷰어로 로드할 수 없습니다. 그리고 악시:뷰어가 처음에 외부 비디오와 함께 로드된 경우 외부 비디오만 사용하여 계속 작업해야 합니다.

외부 비디오를 사용하여 작업할 때 뷰어는 재생 수정자의 값을 무시하고 외부 비디오 확장자에서 재생 유형을 감지합니다. 외부 비디오 URL이 .m3u8로 끝나는 경우 뷰어에서 HLS 재생을 사용하고 있고, 그렇지 않은 경우 점진적 재생이 사용됩니다.
