---
description: 일반 서버 설정
solution: Experience Manager
title: 일반
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 3e4079e7-6def-4938-bb5b-c8122502712d
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 0%

---

# 일반{#general}

일반 서버 설정

## TC::PsPort - 기본 수신 포트 {#section-d31d3051aa994a76b60b70c3d9f7e89f}

에 대한 기본 수신 포트를 지정합니다. [!DNL Platform Server]. 이 포트는 이미지 제공, 이미지 렌더링 및 Dynamic Media 뷰어(설치된 경우)에 대한 설명서 및 예제 페이지에 액세스하는 데에도 사용됩니다.

## IS::CacheServerUrl - 서비스 루트 Url 캐싱 {#section-bcca227a1f91453b834db4ea050968e2}

이미지 서버가 캐싱 서비스에 액세스할 수 있도록 허용하는 HTTP 루트 경로를 지정합니다. 을(를) 로 설정해야 합니다. [!DNL http://localhost:TC::PsPort /is/cache/secondary], 포트 번호가 일치하는 경우 `TC::PsPort`.

## IS::RemoteUrlDefaultExpiration - 원격 Image Source 기본 TTL {#section-e4c31228b459492cacd2f482d9575f71}

를 사용하여 원격 소스에서 HTTP를 통해 얻은 캐시된 이미지의 TTL입니다 `src={…}` 구성합니다. 원격 서버가 HTTP 응답에 만료 헤더를 포함하지 않는 경우에만 사용됩니다. 정수 값(초)입니다.

## IS::RemoteUrlTimeout - 원격 Image Source 시간 초과 {#section-437646c479cc4bea81dae42100a3c50a}

이미지 서버가 HTTP를 통해 요청한 이미지 파일을 제공할 때까지 기다린 후에 오류를 반환합니다. 정수 값(초)입니다.

## PS::allowDefaultCatalogRequests - 기본 카탈로그 요청 활성화/비활성화 {#section-484e442a115a49b4ac269d1718b351e1}

경로에 유효한 카탈로그 ID를 포함하지 않는 요청을 허용하지 않도록 false로 설정합니다. 기본값은 입니다. `true`. 로 설정된 경우 `false`: 카탈로그 id가 없는 요청에 대해 오류가 반환됩니다.

>[!NOTE]
>
>`req=catalogprops` 은 이 설정의 대상이 아닙니다.

## PS::saveToFile.saveTimeout - 파일 저장 시간 초과 {#section-d22afd8ad86144b28684ed95a59db40e}

에 대한 기본 시간 초과 값 `req=saveToFile` when `timeout=`이 지정되지 않았습니다. `msec`. 지정된 시간 내에 저장 작업이 완료되지 않으면 오류가 반환됩니다.
