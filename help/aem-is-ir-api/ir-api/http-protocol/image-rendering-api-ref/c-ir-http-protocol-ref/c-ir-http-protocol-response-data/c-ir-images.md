---
description: 요청이 성공적으로 완료되면 이미지 데이터가 반환되고, 요청에 req= 명령이 포함되어 있지 않거나, req=에 img 값 중 하나가 있는 경우, debug
solution: Experience Manager
title: 이미지
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 089aaf9d-f414-4ca4-9d6d-7f429de2531e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 1%

---

# 이미지{#images}

요청이 성공적으로 완료되고 요청에 req= 명령이 포함되지 않거나 req= 값 중 하나가 있는 경우 이미지 데이터가 반환됩니다.img, debug

HTTP 응답 MIME 유형은 `fmt=`에 의해 결정되거나, `fmt=`이 지정되지 않은 경우 `attribute::Format` 값에 따라 다릅니다.

요청 메서드가 무조건적 `GET` 또는 `HEAD`인 경우 HTTP 응답 상태가 &#39;200 OK&#39;입니다.

서버는 상태 &#39;304&#39;(수정되지 않음)로 응답하고 조건 `GET` 요청(`request-header`에 있는 [!DNL If-Modified-Since] 필드 사용)에 응답하여 이미지 데이터를 반환하지 않을 수 있습니다.
