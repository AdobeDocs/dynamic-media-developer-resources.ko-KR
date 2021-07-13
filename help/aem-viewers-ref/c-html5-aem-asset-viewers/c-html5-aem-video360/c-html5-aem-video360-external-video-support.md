---
description: 뷰어는 Dynamic Media Classic 또는 AEM Dynamic Media 외부에서 호스팅되는 비디오 재생을 지원합니다.
solution: Experience Manager
title: 외부 비디오 지원
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR 비디오
role: Developer,User
exl-id: b592f03b-92ab-47d8-96a6-87982fedc901
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 0%

---

# 외부 비디오 지원{#external-video-support}

뷰어는 Dynamic Media Classic 또는 AEM Dynamic Media 외부에서 호스팅되는 비디오 재생을 지원합니다.

외부 비디오에 대해 지원되는 형식은 H.264 형식의 MP4 또는 HLS 스트림에 대한 M3U8 매니페스트입니다.

뷰어는 Dynamic Media Classic 또는 AEM Dynamic Media 비디오 또는 외부 비디오에서 작동할 수 있습니다. 뷰어가 Dynamic Media Classic/AEM Dynamic Media 비디오으로 시작하는 경우 앞으로 이러한 자산 유형과 함께 사용해야 합니다. [setVideo](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) 메서드를 사용하여 외부 비디오를 이 뷰어에 로드할 수 없고 그 반대의 경우도 가능합니다. 즉, 뷰어가 처음에 외부 비디오와 함께 로드되었을 경우 외부 비디오에서만 계속 작동합니다.

외부 비디오로 작업할 때 뷰어는 모든 재생 수정자의 값을 무시하고 외부 비디오 확장에서 재생 유형을 감지합니다. 외부 비디오 URL이 `.m3u8`로 끝나는 경우 뷰어는 HLS 재생을 사용하고 있습니다. 그렇지 않으면 점진적 재생이 사용됩니다.
