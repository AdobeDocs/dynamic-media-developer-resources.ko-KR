---
description: 이러한 서버 설정을 사용하여 오류를 리디렉션합니다.
seo-description: 이러한 서버 설정을 사용하여 오류를 리디렉션합니다.
seo-title: 오류 리디렉션
solution: Experience Manager
title: 오류 리디렉션
topic: Scene7 Image Serving - Image Rendering API
uuid: b2c2f725-98c3-44a4-8f50-2ca4da7f2156
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 오류 리디렉션{#error-redirection}

이러한 서버 설정을 사용하여 오류를 리디렉션합니다.

>[!NOTE]
>
>네트 경로의 파이프 문자(|)는 오류 리디렉션에 대해 지원되지 않습니다.

## PS::errorRedirect.rootUrl - 리디렉션 서버 {#section-85f22e48d68842a490b0e1191543b558}

루트 URL( [!DNL HTTP:// *[!DNL domain]*[:[ *[!DNL port]*]) 로컬에서 실패한 요청을 리디렉션하는 보조 이미지 제공 배포용. 이 설정이 비어 있거나 정의되지 않은 경우 오류 리디렉션이 비활성화되었습니다(기본값).

## PS::errorRedirect.connectTimeout - 리디렉션 연결 시간 초과 {#section-3971be8f720d4b32a2cc7860b4085971}

서버에 오류가 반환되기 전에 서버가 보조 서버와의 연결을 설정할 때까지 최대 시간(밀리초)입니다.

## PS::errorRedirect.socketTimeout - 리디렉션 응답 시간 초과 {#section-69d8579f748d4044bca99dfb64dd523c}

서버가 리디렉션 요청을 취소하고 클라이언트에 오류를 반환하기 전에 보조 서버가 데이터를 반환할 때까지 최대 시간(밀리초)입니다.
