---
title: 이미지
description: 요청이 성공적으로 완료되면 이미지 데이터가 반환되고, 요청에 req= 명령이 포함되어 있지 않거나, req=에 img 값 중 하나가 있는 경우, debug
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 089aaf9d-f414-4ca4-9d6d-7f429de2531e
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 1%

---

# 이미지{#images}

요청이 성공적으로 완료되고 요청에 req= 명령이 포함되지 않거나 req= 값 중 하나가 있는 경우 이미지 데이터가 반환됩니다. img, debug

HTTP 응답 MIME 유형은 `fmt=`또는 if `fmt=` 이 지정되지 않은 경우, 이 값은 `attribute::Format`.

요청 메서드가 무조건인 경우 HTTP 응답 상태가 &#39;200 OK&#39;입니다 `GET` 또는 `HEAD`.

서버는 상태가 &#39;304&#39;(수정되지 않음)인 응답을 할 수 있으며, 조건부 응답으로 이미지 데이터를 반환하지 않을 수 있습니다 `GET` 요청(다음 포함) [!DNL If-Modified-Since] 에 있는 필드 `request-header`).
