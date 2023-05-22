---
title: 이미지
description: 요청이 성공적으로 완료되고 요청에 req= 명령이 포함되지 않았거나 req=에 다음 값 중 하나가 있으면 이미지 데이터가 반환됩니다.
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

요청이 성공적으로 완료되고 요청에 req= 명령이 포함되지 않았거나 req=에 다음 값 중 하나가 있는 경우 이미지 데이터가 반환됩니다. img, debug

HTTP 응답 MIME 유형은 다음을 통해 결정됩니다. `fmt=`, 또는, `fmt=` 이 지정되지 않은 경우 값 `attribute::Format`.

요청 메서드가 무조건인 경우 HTTP 응답 상태는 &#39;200 OK&#39;입니다. `GET` 또는 `HEAD`.

서버는 상태 &#39;304&#39;(수정되지 않음)로 응답하고 조건에 대한 응답으로 이미지 데이터를 반환하지 않을 수 있습니다 `GET` 요청(포함) [!DNL If-Modified-Since] 필드 위치: `request-header`).
