---
description: 일반 서버 설정
solution: Experience Manager
title: 일반
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 3e4079e7-6def-4938-bb5b-c8122502712d
TQID: 'https://experienceleague.adobe.com/hjww7EYpf4xNxpUFQ1fudMOqNtokgykthwhonn78ZFE'
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
source-wordcount: 227
ht-degree: 0%

---

# 일반{#general}

일반 서버 설정

## TC::PsPort - 기본 수신 포트 {#section-d31d3051aa994a76b60b70c3d9f7e89f}

[!DNL Platform Server]에 대한 기본 수신 대기 포트를 지정합니다. 이 포트는 이미지 제공, 이미지 렌더링 및 Dynamic Media 뷰어(설치된 경우)에 대한 설명서 및 예제 페이지에 액세스하는 데에도 사용됩니다.

## IS::CacheServerUrl - 캐싱 서비스 루트 Url {#section-bcca227a1f91453b834db4ea050968e2}

이미지 서버가 캐싱 서비스에 액세스할 수 있도록 하는 HTTP 루트 경로를 지정합니다. 포트 번호가 `TC::PsPort`과(와) 일치하는 [!DNL http://localhost:TC::PsPort /is/cache/secondary]&#x200B;(으)로 설정해야 합니다.

## IS::RemoteUrlDefaultExpiration - 원격 Image Source 기본 TTL {#section-e4c31228b459492cacd2f482d9575f71}

`src={…}` 구문을 사용하여 원격 원본에서 HTTP를 통해 얻은 캐시된 이미지의 TTL입니다. 원격 서버의 HTTP 응답에 만료 헤더가 포함되지 않은 경우에만 사용됩니다. 정수 값(초)입니다.

## IS::RemoteUrlTimeout - 원격 Image Source 시간 초과 {#section-437646c479cc4bea81dae42100a3c50a}

이미지 서버가 오류를 반환하기 전에 HTTP를 통해 요청된 이미지 파일을 원격 서버가 전달할 때까지 대기하는 시간입니다. 정수 값(초)입니다.

## PS::allowDefaultCatalogRequests - 기본 카탈로그 요청 활성화/비활성화 {#section-484e442a115a49b4ac269d1718b351e1}

경로에 유효한 카탈로그 ID가 포함되지 않은 요청을 허용하지 않으려면 false로 설정하십시오. 기본값은 `true`입니다. `false`(으)로 설정된 경우 카탈로그 ID가 없는 요청에 대해 오류가 반환됩니다.

>[!NOTE]
>
>`req=catalogprops`은(는) 이 설정의 적용을 받지 않습니다.

## PS::saveToFile.saveTimeout - 파일 저장 시간 초과 {#section-d22afd8ad86144b28684ed95a59db40e}

`timeout=`이(가) 지정되지 않은 경우 `req=saveToFile`의 기본 시간 초과 값입니다. `msec`. 지정된 시간 내에 저장 작업이 완료되지 않으면 오류가 반환됩니다.
