---
description: 서버 캐시에 이 서버 설정을 사용합니다.
solution: Experience Manager
title: 서버 캐시
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 0%

---


# 서버 캐시{#server-caches}

서버 캐시에 이 서버 설정을 사용합니다.

## PS::cache.rootPaths - 캐시 데이터 폴더 {#section-f0aa808304d74ecdb0c3644f11906c53}

플랫폼 서버의 디스크 캐시에 대한 루트 폴더입니다. *[!DNL install_folder]*&#x200B;에 상대적인 하나 이상의 절대 파일 경로 또는 경로는 세미콜론(;)으로 구분되어 있습니다. HTTP 응답 캐시에 대한 데이터는 지정된 모든 폴더에 고르게 배포됩니다. 보조 캐시에 대한 캐시(컴파일된 이미지 카탈로그 및 외부 이미지 데이터)는 기본 캐시 폴더(목록의 첫 번째 폴더)에 배치됩니다.

## PS::cache.maxSize - 응답 데이터 캐시 크기 {#section-ed2e1e7ba4bd4e13b77bb20c4cacddb4}

HTTP 응답 캐시의 최대 크기(바이트)입니다. 이 설정은 캐시할 실제 데이터의 양을 제한합니다.파일 시스템 오버헤드를 고려하지 않습니다. ([응답 데이터 캐시](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-data-caches/c-response-data-cache.md#concept-81ea996c242441f2a69f7e9d9b3a29ca)를 참조하십시오.) 캐시 데이터 폴더가 여러 개 지정된 경우 캐시 데이터가 모든 폴더에 고르게 분산됩니다. [!DNL PlatformServer.conf]의 `cache.maxSize` 값은 바이트 단위입니다.

## PS::cache.maxEntries - 응답 데이터 캐시 최대 항목 {#section-5603e327e90542a5b50aeeb27b080410}

메모리 내 HTTP 응답 캐시 인덱스에 할당된 항목 수입니다.

>[!NOTE]
>
>Linux에서 i-nodes가 부족하지 않도록 캐시 파티션에 충분한 i-nodes가 할당되었는지 확인합니다.

## IS::TempDirectory - 이미지 서버 임시 파일 폴더 {#section-42ea1e7a68c444878f7245c5bbcb1672}

이미지 서버는 중간 데이터를 디스크에 저장해야 하는 경우가 있습니다. 경로는 절대 경로이거나 *[!DNL install_folder]*&#x200B;에 상대적인 경로일 수 있습니다.

>[!NOTE]
>
>이 설정을 변경하기 전에 새 폴더를 만들어야 합니다. 이미지 서버가 폴더를 완전히 제어할 수 있도록 액세스 권한이 설정되어 있는지 확인합니다.

## SV::temp - 서버 관리자 임시 파일 폴더 {#section-fd2cd5ef7e814a4bb56aaf5525e1a154}

중간 데이터를 디스크에 저장해야 하는 경우가 있습니다. 경로는 절대 경로이거나 *[!DNL install_folder]*&#x200B;에 상대적인 경로일 수 있습니다. 기본값은 [!DNL *[!DNL install_folder]*/temp]입니다.

>[!NOTE]
>
>이 설정을 변경하기 전에 새 폴더를 만들어야 합니다. 서버 관리자가 폴더를 완전히 제어할 수 있도록 액세스 권한이 설정되어 있는지 확인합니다.

