---
description: 요청이 성공적으로 완료되면 이미지 데이터가 반환되고 요청에 req= 명령이 포함되어 있지 않거나, req=img 또는 req=tmb인 경우 이미지 데이터가 반환됩니다.
solution: Experience Manager
title: 이미지
feature: Dynamic Media Classic,SDK/API
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 1%

---


# 이미지{#images}

요청이 성공적으로 완료되면 이미지 데이터가 반환되고 요청에 req= 명령이 포함되어 있지 않거나, req=img 또는 req=tmb인 경우 이미지 데이터가 반환됩니다.

HTTP 응답 MIME 유형은 `fmt=`으로 결정되거나, `fmt=`이 지정되지 않은 경우 `<image/jpeg>`입니다.

요청 메서드가 무조건적인 `GET` 또는 `HEAD`인 경우 HTTP 응답 상태는 &#39;200 OK&#39;입니다.

서버는 상태 &#39;304&#39;(수정되지 않음)로 응답하고 조건 `GET` 요청에 대한 응답으로 이미지 데이터를 반환하지 않을 수 있습니다(유효한 `If-Modified-Since` 또는 `If-None-Match` 헤더를 포함).
