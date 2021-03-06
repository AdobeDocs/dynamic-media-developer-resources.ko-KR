---
description: IS 서버는 성공적으로 열거나 읽을 수 없는 소스 이미지가 포함된 요청에 대해 대체 서버로 페일오버하도록 구성할 수 있습니다.
solution: Experience Manager
title: 오류 시 리디렉션
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c5541bf3-3296-4ce3-a2ff-9f6336f78ea9
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '299'
ht-degree: 0%

---

# 오류 시 리디렉션{#redirect-on-error}

IS 서버는 성공적으로 열거나 읽을 수 없는 소스 이미지가 포함된 요청에 대해 대체 서버로 페일오버하도록 구성할 수 있습니다.

다음 유형의 요청은 리디렉션됩니다.

* IS 이미지는 카탈로그에 있지만 디스크에 없습니다.

   이미지가 카탈로그에 없으면 이미지를 찾을 수 없을 때 오류 리디렉션이 발생하지 않아야 합니다.

* 이미지, 색상 프로필 또는 글꼴이 손상되었습니다.
* 정적 콘텐츠를 디스크에서 찾을 수 없습니다.

   참조된 정적 콘텐츠에 카탈로그 레코드가 없는 경우에도 정적 콘텐츠 요청을 디스크에서 찾을 수 없으면 리디렉션됩니다.

다른 경우에는 오류 리디렉션이 발생하지 않습니다.

활성화되고 요청을 처리하는 동안 이러한 오류가 발생하면 주 서버가 처리를 위해 보조 서버에 요청을 전송합니다. 성공 또는 실패 여부에 관계없이 응답이 클라이언트에 직접 전달됩니다. 주 서버는 캐시 사용을 사용하여 전달된 요청의 로그 항목을 표시합니다 `REMOTE`. 응답 데이터가 주 서버에 의해 로컬로 캐시되지 않습니다.

오류 리디렉션은 `PS::errorRedirect.rootUrl` 을 눌러 보조 서버의 HTTP 도메인 이름 및 포트 번호를 지정합니다. 또한 연결 시간 초과는 `PS::errorRedirect.connectTimeout` 그리고 주 서버가 보조 서버의 응답을 기다리는 최대 시간 동안 오류가 클라이언트에 반환될 때까지 `PS::errorRedirect.socketTimeout`.

>[!NOTE]
>
>보조 서버에 연결할 수 없으면 기본 이미지나 오류 이미지가 구성된 경우에도 텍스트 오류 응답이 클라이언트에 반환됩니다.

>[!NOTE]
>
>네트 경로의 파이프 문자(|)는 오류 리디렉션을 지원하지 않습니다.

## 참조 {#section-2e8bfc128b944baf8108279d16492f3f}

[오류 리디렉션](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-error-redirection.md#reference-268b1bf6ce1b44bb979727c6f5daf1ac)
