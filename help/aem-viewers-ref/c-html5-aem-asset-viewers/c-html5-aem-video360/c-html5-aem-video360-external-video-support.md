---
description: 뷰어는 SPS 또는 AEM Dynamic Media 외부에서 호스팅되는 비디오 재생을 지원합니다.
seo-description: 뷰어는 SPS 또는 AEM Dynamic Media 외부에서 호스팅되는 비디오 재생을 지원합니다.
seo-title: 외부 비디오 지원
solution: Experience Manager
title: 외부 비디오 지원
topic: Dynamic media
uuid: 2e9f1c54-627f-4462-ae85-8a5ca1d09762
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---


# 외부 비디오 지원{#external-video-support}

뷰어는 SPS 또는 AEM Dynamic Media 외부에서 호스팅되는 비디오 재생을 지원합니다.

외부 비디오에 대해 지원되는 형식은 H.264 형식의 MP4 또는 HLS 스트림에 대한 M3U8 매니페스트입니다.

뷰어는 Dynamic Media Classic 또는 AEM Dynamic Media 비디오나 외부 비디오에서 사용할 수 있습니다. 뷰어가 Dynamic Media Classic/AEM Dynamic Media 비디오으로 시작하는 경우 앞으로 이와 같은 자산 유형과 함께 사용해야 합니다. [setVideo](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) 메서드를 사용하여 외부 비디오를 이 뷰어에 로드할 수 없으며 그 반대의 경우도 가능합니다. 즉, 뷰어가 처음에 외부 비디오로 로드되었더라도 외부 비디오만 계속 작동합니다.

외부 비디오를 사용하여 작업할 때 뷰어는 모든 재생 수정자의 값을 무시하고 외부 비디오 확장자에서 재생 유형을 감지합니다. 외부 비디오 URL이 `.m3u8`으로 끝나는 경우 뷰어는 HLS 재생을 사용합니다.그렇지 않으면 점진적 재생이 사용됩니다.
