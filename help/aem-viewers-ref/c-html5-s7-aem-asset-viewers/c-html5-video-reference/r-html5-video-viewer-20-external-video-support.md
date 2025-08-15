---
title: 외부 비디오 지원
description: 뷰어는 Dynamic Media Classic 또는 Adobe Experience Manager - Dynamic Media 외부에서 호스팅되는 비디오 재생을 지원합니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: b42e67cb-6959-4eea-8d45-49481e0e9d80
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 0%

---

# 외부 비디오 지원{#external-video-support}

뷰어는 Dynamic Media Classic 또는 Adobe Experience Manager - Dynamic Media 외부에서 호스팅되는 비디오 재생을 지원합니다.

외부 비디오에 지원되는 형식은 H.264 형식의 MP4 또는 HLS 스트림에 대한 M3U8 매니페스트입니다.

뷰어는 Dynamic Media Classic 또는 Experience Manager - Dynamic Media 비디오 또는 외부 비디오와 함께 작동할 수 있습니다. 뷰어가 Dynamic Media Classic/Dynamic Media 비디오로 시작하는 경우 해당 에셋 유형을 계속 사용하면 [`setVideo`](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) 메서드를 사용하여 외부 비디오를 이 뷰어로 로드할 수 없습니다. 그리고 다른 예: 뷰어가 처음에 외부 비디오로 로드된 경우, 외부 비디오로만 계속 작업해야 합니다.

외부 비디오로 작업할 때 뷰어는 재생 수정자 값을 무시하고 외부 비디오 확장에서 재생 유형을 감지합니다. 외부 비디오 URL이 `.m3u8`(으)로 끝나는 경우 뷰어가 HLS 재생을 사용하고, 그렇지 않은 경우 점진적 재생이 사용됩니다.
