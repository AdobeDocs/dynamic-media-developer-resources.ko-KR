---
description: 마지막으로 수정한 응답 헤더를 활성화합니다. 이미지 제공에서 방출하는 캐시 가능한 HTTP 응답에 마지막으로 수정한 헤더를 포함하거나 비활성화합니다.
seo-description: 마지막으로 수정한 응답 헤더를 활성화합니다. 이미지 제공에서 방출하는 캐시 가능한 HTTP 응답에 마지막으로 수정한 헤더를 포함하거나 비활성화합니다.
seo-title: UseLastModified
solution: Experience Manager
title: UseLastModified
topic: Scene7 Image Serving - Image Rendering API
uuid: 9dae4f15-4323-4f68-917f-6d72ae52c753
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 1%

---


# UseLastModified{#uselastmodified}

마지막으로 수정한 응답 헤더를 활성화합니다. 이미지 제공에서 방출하는 캐시 가능한 HTTP 응답에 마지막으로 수정한 헤더를 포함하거나 비활성화합니다.

서버는 응답에 포함된 모든 카탈로그/카탈로그 레코드의 최신 `catalog::TimeStamp` 값을 마지막으로 수정한 헤더 값으로 사용합니다.

전송 헤더를 지원하지 않는 분산 캐싱 네트워크 또는 기타 캐싱 시스템이 사용되는 경우에만 활성화되어야 합니다.

>[!NOTE]
>
>여러 이미지 제공 호스트가 포함된 로드 밸런싱된 환경에서 마지막으로 수정한 헤더를 사용할 때는 주의해야 합니다. 서버에 동일한 카탈로그 항목에 대한 타임스탬프가 다른 경우 클라이언트 캐싱이 실패하여 서버 로드가 증가할 수 있습니다. 이러한 상황은 다음과 같이 발생할 수 있습니다.
>
>* `catalog::TimeStamp` 및 `attribute::TimeStamp` 모두 아니므로 [!DNL catalog.ini] 파일의 수정 시간이 `catalog::TimeStamp`의 기본값으로 사용됩니다.
   >
   >
* 네트워크 마운트를 통해 이미지 카탈로그 파일을 공유하는 대신 각 서버에는 로컬 파일 시스템에 카탈로그 파일의 자체 인스턴스가 있습니다.
>* 동일한 [!DNL catalog.ini] 파일의 두 개 이상의 인스턴스에 다른 파일 수정 날짜가 있으며, 파일 복사가 잘못되었을 수 있습니다.

>



## 속성 {#section-7e26009b7d0a4a3ab234bf2a37f599e0}

플래그. 비활성화하려면 0, 마지막으로 수정한 HTTP 헤더를 활성화하려면 1.

## 기본값 {#section-4eb47aadab8b41609bef296a4115f9f4}

정의되지 않았거나 비어 있는 경우 `default::UseLastModified`에서 상속됩니다.

## 참조 {#section-4211a78f8a5b45629c62fed5ae82f1cb}

[카탈로그::타임스탬프](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
