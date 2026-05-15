---
description: 이러한 서버 설정을 사용하여 오류를 리디렉션합니다.
solution: Experience Manager
title: 오류 리디렉션
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: a184e113-9708-412f-9b71-d75a35629adf
TQID: 'https://experienceleague.adobe.com/3fcob7pfE-bMms-4PtD5MKkcolKHmXEWdzEL7vgzLhc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 0%

---

# 오류 리디렉션{#error-redirection}

이러한 서버 설정을 사용하여 오류를 리디렉션합니다.

>[!NOTE]
>
>오류 리디렉션에 대해 네트 경로의 파이프 문자(|)가 지원되지 않습니다.

## PS::errorRedirect.rootUrl - 리디렉션 서버 {#section-85f22e48d68842a490b0e1191543b558}

로컬에서 실패한 요청을 리디렉션해야 하는 2차 이미지 서비스 배포의 루트 URL( HTTP:// *[!DNL domain]*[: *[!DNL port]*])입니다. 이 설정이 비어 있거나 정의되지 않으면 오류 리디렉션이 비활성화됩니다(기본값).

## PS::errorRedirect.connectTimeout - 리디렉션 연결 시간 초과 {#section-3971be8f720d4b32a2cc7860b4085971}

서버에 오류가 클라이언트에 반환되기 전에 보조 서버와의 연결이 설정될 때까지 서버가 대기하는 최대 시간(밀리초)입니다.

## PS::errorRedirect.socketTimeout - 리디렉션 응답 시간 제한 {#section-69d8579f748d4044bca99dfb64dd523c}

리디렉션 요청을 중단하고 클라이언트에 오류를 반환하기 전에 보조 서버가 데이터를 반환할 때까지 서버가 대기하는 최대 시간(밀리초)입니다.
