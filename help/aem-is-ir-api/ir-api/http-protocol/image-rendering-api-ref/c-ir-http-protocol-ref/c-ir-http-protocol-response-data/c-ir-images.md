---
description: 요청이 성공적으로 완료되면 이미지 데이터가 반환되고 요청에 req= 명령이 포함되어 있지 않거나 req=에 img 값 중 하나가 있는 경우, debug
seo-description: 요청이 성공적으로 완료되면 이미지 데이터가 반환되고 요청에 req= 명령이 포함되어 있지 않거나 req=에 img 값 중 하나가 있는 경우, debug
seo-title: 이미지
solution: Experience Manager
title: 이미지
topic: Scene7 Image Serving - Image Rendering API
uuid: 8e8c5ec9-dc15-4894-b6a1-8e5241f03977
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 1%

---


# 이미지{#images}

요청이 성공적으로 완료되면 이미지 데이터가 반환되고 요청에 req= 명령이 포함되지 않거나 req=에 다음 값 중 하나가 있는 경우 이미지 데이터가 반환됩니다.img, debug

HTTP 응답 MIME 유형은 `fmt=`에 의해 결정되거나, `fmt=`이 지정되지 않은 경우 `attribute::Format` 값에 따라 달라집니다.

요청 메서드가 무조건적인 `GET` 또는 `HEAD`인 경우 HTTP 응답 상태는 &#39;200 OK&#39;입니다.

서버는 상태 &#39;304&#39;(수정되지 않음)로 응답하고 조건 `GET` 요청에 대한 응답으로 이미지 데이터를 반환하지 않을 수 있습니다(`request-header`에 [!DNL If-Modified-Since] 필드가 있음).
