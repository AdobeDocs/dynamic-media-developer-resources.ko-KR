---
description: 일반 서버 설정
seo-description: 일반 서버 설정
seo-title: 일반
solution: Experience Manager
title: 일반
topic: Scene7 Image Serving - Image Rendering API
uuid: d7ec3dba-64b8-431b-b446-84ab6139ba8a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 일반{#general}

일반 서버 설정

## TC::PsPort - 기본 의견 수렴 포트 {#section-d31d3051aa994a76b60b70c3d9f7e89f}

플랫폼 서버의 기본 수신 포트를 지정합니다. 이 포트는 이미지 제공, 이미지 렌더링 및 Scene7 뷰어(설치된 경우)에 대한 설명서 및 예제 페이지에 액세스하는 데 사용됩니다.

## IS::CacheServerUrl - Caching Service Root Url {#section-bcca227a1f91453b834db4ea050968e2}

이미지 서버가 캐싱 서비스에 액세스할 수 있도록 HTTP 루트 경로를 지정합니다. 포트 번호와 일치하는 [!DNL http://localhost:TC::PsPort /is/cache/secondary]로 설정해야 합니다 `TC::PsPort`.

## IS::RemoteUrlDefaultExpiration - Remote Image Source Default TTL {#section-e4c31228b459492cacd2f482d9575f71}

구조를 사용하여 원격 소스에서 HTTP를 통해 얻은 캐시된 이미지의 TTL입니다. `src={…}` 원격 서버가 HTTP 응답에 만료 헤더를 포함하지 않는 경우에만 사용됩니다. 정수 값(초)입니다.

## IS::RemoteUrlTimeout - 원격 이미지 소스 시간 초과 {#section-437646c479cc4bea81dae42100a3c50a}

이미지 서버가 원격 서버가 HTTP를 통해 요청한 이미지 파일을 제공할 때까지 기다린 후 오류를 반환합니다. 정수 값(초)입니다.

## PS::allowDefaultCatalogRequests - 기본 카탈로그 요청 활성화/비활성화 {#section-484e442a115a49b4ac269d1718b351e1}

경로에 유효한 카탈로그 ID를 포함하지 않는 요청을 허용하지 않으려면 false로 설정합니다. Default is `true`. 로 설정하면 카탈로그 ID가 없는 요청에 대해 `false`오류가 반환됩니다.

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>`req=catalogprops` 은 이 설정의 대상이 아닙니다.

## PS::saveToFile.saveTimeout - 파일 저장 시간 초과 {#section-d22afd8ad86144b28684ed95a59db40e}

Default timeout value for `req=saveToFile` when `timeout=`is not specified. `msec`. 저장 작업이 지정된 시간 내에 완료되지 않으면 오류가 반환됩니다.
