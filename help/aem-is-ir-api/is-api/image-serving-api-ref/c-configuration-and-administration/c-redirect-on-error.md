---
description: IS 서버는 열거나 성공적으로 읽을 수 없는 소스 이미지를 포함하는 요청에 대해 대체 서버로 장애 조치(failover)하도록 구성할 수 있습니다.
solution: Experience Manager
title: 오류 시 리디렉션
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c5541bf3-3296-4ce3-a2ff-9f6336f78ea9
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# 오류 시 리디렉션{#redirect-on-error}

IS 서버는 열거나 성공적으로 읽을 수 없는 소스 이미지를 포함하는 요청에 대해 대체 서버로 장애 조치(failover)하도록 구성할 수 있습니다.

다음 유형의 요청이 리디렉션됩니다.

* 카탈로그에는 있지만 디스크에는 없는 IS 이미지.

  이미지가 카탈로그에 없으면 이미지를 찾을 수 없을 때 오류 리디렉션이 발생하지 않습니다.

* 이미지, 색상 프로파일 또는 글꼴이 손상되었습니다.
* 디스크에서 정적 콘텐츠를 찾을 수 없습니다.

  정적 콘텐츠 요청은 참조된 정적 콘텐츠에 카탈로그 레코드가 없는 경우에도 디스크에서 찾을 수 없으면 리디렉션됩니다.

다른 경우에는 오류 리디렉션이 발생하지 않습니다.

활성화된 경우 및 요청을 처리하는 동안 이러한 오류가 발생하면 주 서버가 처리를 위해 보조 서버에 요청을 전송합니다. 성공 또는 실패를 나타내는지에 관계없이 응답은 클라이언트에 직접 전달됩니다. 주 서버는 전달된 요청의 로그 항목을 캐시 사용으로 표시합니다 `REMOTE`. 응답 데이터는 주 서버에서 로컬로 캐시되지 않습니다.

오류 리디렉션은 설정에 의해 활성화됩니다. `PS::errorRedirect.rootUrl` 보조 서버의 HTTP 도메인 이름 및 포트 번호. 또한 연결 시간 초과는 `PS::errorRedirect.connectTimeout` 주 서버가 클라이언트에 오류를 반환하기 전에 보조 서버의 응답을 기다리는 최대 시간 `PS::errorRedirect.socketTimeout`.

>[!NOTE]
>
>보조 서버에 연결할 수 없는 경우 기본 이미지 또는 오류 이미지가 구성되어 있더라도 텍스트 오류 응답이 클라이언트에 반환됩니다.

>[!NOTE]
>
>오류 리디렉션에 대해 네트 경로의 파이프 문자(|)가 지원되지 않습니다.

## 참조 {#section-2e8bfc128b944baf8108279d16492f3f}

[오류 리디렉션](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-error-redirection.md#reference-268b1bf6ce1b44bb979727c6f5daf1ac)
