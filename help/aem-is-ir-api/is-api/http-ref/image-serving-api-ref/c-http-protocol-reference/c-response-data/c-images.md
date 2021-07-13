---
description: 요청이 성공적으로 완료되면 이미지 데이터가 반환되고, 요청에 req= 명령이 포함되어 있지 않거나 req=img 또는 req=tmb인 경우 반환됩니다.
solution: Experience Manager
title: 이미지
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3aa46d48-82eb-4a21-a5e5-b33904b97888
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 1%

---

# 이미지{#images}

요청이 성공적으로 완료되면 이미지 데이터가 반환되고, 요청에 req= 명령이 포함되어 있지 않거나 req=img 또는 req=tmb인 경우 반환됩니다.

HTTP 응답 MIME 유형은 `fmt=`에 의해 결정되거나, `fmt=`을 지정하지 않으면 `<image/jpeg>`입니다.

요청 메서드가 무조건적 `GET` 또는 `HEAD`인 경우 HTTP 응답 상태가 &#39;200 OK&#39;입니다.

서버는 상태 &#39;304&#39;(수정되지 않음)로 응답하고 조건부 `GET` 요청(유효한 `If-Modified-Since` 또는 `If-None-Match` 헤더를 포함함)에 응답하여 이미지 데이터를 반환하지 않을 수 있습니다.
