---
description: 요청이 성공적으로 완료되면 이미지 데이터가 반환됩니다. 요청에 req= 명령이 포함되어 있지 않거나 req=img 또는 req=tmb인 경우 이미지 데이터가 반환됩니다.
seo-description: 요청이 성공적으로 완료되면 이미지 데이터가 반환됩니다. 요청에 req= 명령이 포함되어 있지 않거나 req=img 또는 req=tmb인 경우 이미지 데이터가 반환됩니다.
seo-title: 이미지
solution: Experience Manager
title: 이미지
topic: Scene7 Image Serving - Image Rendering API
uuid: 715154b6-f9ac-459e-a566-f78a4ca4580d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 이미지{#images}

요청이 성공적으로 완료되면 이미지 데이터가 반환됩니다. 요청에 req= 명령이 포함되어 있지 않거나 req=img 또는 req=tmb인 경우 이미지 데이터가 반환됩니다.

HTTP 응답 MIME 유형은 `fmt=`또는 지정하지 `fmt=` 않은 경우 에 의해 결정됩니다 `<image/jpeg>`.

요청 메서드가 무조건 `GET` 또는 `HEAD`인 경우 HTTP 응답 상태는 &#39;200 OK&#39;입니다.

서버는 상태 &#39;304&#39;(수정되지 않음)로 응답하고 조건 `GET` 요청에 대한 응답으로 이미지 데이터를 반환하지 않을 수 있습니다(유효한 `If-Modified-Since` 또는 `If-None-Match` 헤더를 포함).
