---
title: 외부 비디오 지원
description: 뷰어는 Dynamic Media Classic 또는 Adobe Experience Manager - Dynamic Media 외부에서 호스팅되는 비디오 재생을 지원합니다.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 2ab5a083-5995-440a-a9a6-6642277b8a58
TQID: 'https://experienceleague.adobe.com/nLVjtwe8hj5YpMX6M1GKt1Fx-tZK2Qxe1kdWcK8BQPw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
  - id: d09181b5-a36a-43de-ba01-36641440bc43
    internal-label: Experience Manager Assets
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
  - id: fe490c45-63fa-5b99-b5b4-d8cfeda8aa7d
    internal-label: SDK/API
  - id: bd0d2470-932c-4269-8eca-6d939b72d9ef
    internal-label: Dynamic Media
  - id: d4b6216b-4a89-4ff0-8ac0-5a699ba23100
    internal-label: Images and videos
subfeature_v2:
  - id: c12bda38-aa1a-4647-b62e-42cd4537dac6
    internal-label: Dynamic Media Classic
  - id: d17d085a-e808-49dd-b9a6-85a996b999bd
    internal-label: Viewers
  - id: a0cde32c-c339-4649-bd06-f1111bc952fc
    internal-label: Smart Crop
  - id: cb04d42d-1b70-43b0-9951-45998eb6e842
    internal-label: Video
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: 0e24e07f8c91d3e7fda5510ed4252f9953e27467
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 0%
---
# 외부 비디오 지원{#external-video-support}

뷰어는 Dynamic Media Classic 또는 Adobe Experience Manager - Dynamic Media 외부에서 호스팅되는 비디오 재생을 지원합니다.

외부 비디오에 지원되는 형식은 H.264 형식의 MP4 또는 HLS 스트림에 대한 M3U8 매니페스트입니다.

뷰어는 Dynamic Media Classic 또는 Experience Manager - Dynamic Media 비디오 또는 외부 비디오와 함께 작동할 수 있습니다. 뷰어가 Dynamic Media Classic/Dynamic Media 비디오로 시작하는 경우 해당 에셋 유형과 함께 사용하면 다음을 사용하여 외부 비디오를 이 뷰어에 로드할 수 없습니다. [`setVideo`]
(#reference-85d3422d6ce64a36ac74827120b5a17c) 메서드입니다. 그리고 다른 예: 뷰어가 처음에 외부 비디오로 로드된 경우, 외부 비디오로만 계속 작업해야 합니다.

외부 비디오로 작업할 때 뷰어는 재생 수정자 값을 무시하고 외부 비디오 확장에서 재생 유형을 감지합니다. 외부 비디오 URL이 `.M3U8`(으)로 끝나는 경우 뷰어가 HLS 재생을 사용하고, 그렇지 않은 경우 점진적 재생이 사용됩니다.
