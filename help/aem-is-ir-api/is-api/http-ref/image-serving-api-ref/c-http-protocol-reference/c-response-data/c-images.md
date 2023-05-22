---
description: 요청이 성공적으로 완료되고 요청이 req= 명령을 포함하지 않거나 req=img 또는 req=tmb인 경우 이미지 데이터가 반환됩니다.
solution: Experience Manager
title: 이미지
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3aa46d48-82eb-4a21-a5e5-b33904b97888
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 1%

---

# 이미지{#images}

요청이 성공적으로 완료되고 요청이 req= 명령을 포함하지 않거나 req=img 또는 req=tmb인 경우 이미지 데이터가 반환됩니다.

HTTP 응답 MIME 유형은 다음을 통해 결정됩니다. `fmt=`, 또는, `fmt=` 이(가) 지정되지 않았습니다. 이(가) `<image/jpeg>`.

요청 메서드가 무조건인 경우 HTTP 응답 상태는 &#39;200 OK&#39;입니다. `GET` 또는 `HEAD`.

서버는 상태 &#39;304&#39;(수정되지 않음)로 응답하고 조건에 대한 응답으로 이미지 데이터를 반환하지 않을 수 있습니다 `GET` 요청(유효한 요청 포함) `If-Modified-Since` 또는 `If-None-Match` header).
