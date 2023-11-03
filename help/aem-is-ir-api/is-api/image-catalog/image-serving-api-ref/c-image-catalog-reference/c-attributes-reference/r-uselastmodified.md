---
description: 마지막으로 수정된 응답 헤더를 활성화합니다. 이미지 제공에서 내보낸 캐시 가능한 HTTP 응답에 마지막 수정 헤더 포함을 활성화하거나 비활성화합니다.
solution: Experience Manager
title: 마지막 수정 날짜 사용
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4908da5d-636e-44d2-bd49-40e01c8b5f79
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 1%

---

# 마지막 수정 날짜 사용{#uselastmodified}

마지막으로 수정된 응답 헤더를 활성화합니다. 이미지 제공에서 내보낸 캐시 가능한 HTTP 응답에 마지막 수정 헤더 포함을 활성화하거나 비활성화합니다.

서버에서 가장 최근 을 사용합니다. `catalog::TimeStamp` 응답에 포함된 모든 카탈로그/카탈로그 레코드의 값을 Last-Modified 헤더 값으로 설정합니다.

ETAG 헤더를 지원하지 않는 분산 캐싱 네트워크 또는 기타 캐싱 시스템을 사용하는 경우에만 활성화해야 합니다.

>[!NOTE]
>
>여러 이미지 제공 호스트가 포함된 로드 밸런싱된 환경에서 마지막으로 수정된 헤더를 사용할 때 주의해야 합니다. 어떤 이유로든 서버에 동일한 카탈로그 항목에 대한 다른 타임스탬프가 있는 경우 클라이언트 캐싱이 중단되고 서버 로드가 증가할 수 있습니다. 이러한 상황은 다음과 같이 발생할 수 있습니다.
>
>* 둘 다 아님 `catalog::TimeStamp` nor `attribute::TimeStamp`, 따라서 의 수정 시간은 [!DNL catalog.ini] 파일은 의 기본값으로 사용됩니다. `catalog::TimeStamp`.
>
>* 네트워크 마운트를 통해 이미지 카탈로그 파일을 공유하는 대신 각 서버에는 로컬 파일 시스템에 있는 고유한 카탈로그 파일 인스턴스가 있습니다.
>* 동일한 인스턴스 2개 이상 [!DNL catalog.ini] 파일의 파일 수정 날짜가 다릅니다. 파일을 잘못 복사했기 때문일 수 있습니다.
>

## 속성 {#section-7e26009b7d0a4a3ab234bf2a37f599e0}

플래그. 비활성화하려면 0을 사용하고, 마지막으로 수정한 HTTP 헤더를 활성화하려면 1을 사용합니다.

## 기본값 {#section-4eb47aadab8b41609bef296a4115f9f4}

상속 위치 `default::UseLastModified` 정의되지 않은 경우 또는 비어 있는 경우.

## 참조 {#section-4211a78f8a5b45629c62fed5ae82f1cb}

[catalog::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
