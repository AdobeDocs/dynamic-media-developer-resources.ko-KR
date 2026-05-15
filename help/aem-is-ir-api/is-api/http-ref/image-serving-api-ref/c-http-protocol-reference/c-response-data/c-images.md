---
description: 요청이 성공적으로 완료되고 요청이 req= 명령을 포함하지 않거나 req=img 또는 req=tmb인 경우 이미지 데이터가 반환됩니다.
solution: Experience Manager
title: 이미지
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3aa46d48-82eb-4a21-a5e5-b33904b97888
TQID: 'https://experienceleague.adobe.com/1tStTbuCLrOG8XrPgOw5qH-VujpHXX8Pt0IWXg9329Y'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 113
ht-degree: 1%

---

# 이미지{#images}

요청이 성공적으로 완료되고 요청이 req= 명령을 포함하지 않거나 req=img 또는 req=tmb인 경우 이미지 데이터가 반환됩니다.

HTTP 응답 MIME 형식은 `fmt=`에 의해 결정되거나 `fmt=`을(를) 지정하지 않으면 `<image/jpeg>`입니다.

요청 메서드가 무조건인 `GET` 또는 `HEAD`인 경우 HTTP 응답 상태는 &#39;200 OK&#39;입니다.

서버가 상태 &#39;304&#39;(수정되지 않음)로 응답하고 조건부 `GET` 요청(올바른 `If-Modified-Since` 또는 `If-None-Match` 헤더 포함)에 대한 응답으로 이미지 데이터를 반환하지 않을 수 있습니다.
