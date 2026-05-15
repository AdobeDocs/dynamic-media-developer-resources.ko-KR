---
title: 이미지
description: 요청이 성공적으로 완료되고 요청에 req= 명령이 포함되지 않았거나 req=에 다음 값 중 하나가 있으면 이미지 데이터가 반환됩니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 089aaf9d-f414-4ca4-9d6d-7f429de2531e
TQID: 'https://experienceleague.adobe.com/4wHyyXX0gxz9ojr5g5Puu5fBhKXo4hZDjyBuVTao3rQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 1%

---

# 이미지{#images}

요청이 성공적으로 완료되고 요청에 req= 명령이 포함되지 않았거나 req=에 다음 값 중 하나가 있는 경우 이미지 데이터가 반환됩니다. img, debug

HTTP 응답 MIME 형식은 `fmt=`에 의해 결정되거나 `fmt=`을(를) 지정하지 않으면 `attribute::Format`의 값에 따라 달라집니다.

요청 메서드가 무조건인 `GET` 또는 `HEAD`인 경우 HTTP 응답 상태는 &#39;200 OK&#39;입니다.

서버는 상태 &#39;304&#39;(수정되지 않음)로 응답하고 조건부 `GET` 요청(`request-header`에 있는 [!DNL If-Modified-Since] 필드 포함)에 대한 응답으로 이미지 데이터를 반환하지 않을 수 있습니다.
