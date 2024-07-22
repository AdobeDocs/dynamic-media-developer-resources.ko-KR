---
description: Digimarc 사용자 정보입니다. Digimarc 포함에 대한 사용자 정보를 지정합니다.
solution: Experience Manager
title: DigimarcId
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac09c8cd-cb68-4b70-b1b4-9d4ca0166c7f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 3%

---

# DigimarcId{#digimarcid}

Digimarc 사용자 정보입니다. Digimarc 포함에 대한 사용자 정보를 지정합니다.

## 속성 {#section-1e11a36d9e0b4bf3858c4ab15fe7a272}

5~6개의 쉼표로 구분된 정수. 세 번째와 네 번째 숫자는 더 이상 사용되지 않습니다.

`creator-id, creator-pin, durability [ , chroma ]`

`creator-id` 및 `creator-pin`은(는) 서비스를 구입할 때 Digimarc에서 제공합니다. 사용하지 않은 값은 비워 두어야 합니다.

`durability`은(는) Digimarc 워터마크 포함 강도를 지정합니다. 1, 2, 3 또는 4일 수 있으며, 1이 가장 약함을 나타내고, 4가 가장 강한 내구성을 나타낸다.

워터마크를 이미지의 색차 데이터로 인코딩하려면 `chroma`을(를) 1로 설정하고, 광도로 인코딩하려면 0(기본값)으로 설정합니다. 이 설정은 회색 음영 이미지를 출력할 때 무시됩니다.

## 기본값 {#section-d6ecb6e95a7b4232bd612834ea49e6bc}

정의되지 않았거나 비어 있는 경우 `default::DigimarcId`에서 상속됩니다.

## 예 {#section-8469ae1c27b4461da3d53fbabc32d3c5}

내구성이 4로 설정된 테스트 Digimarc 작성기 ID를 지정합니다.

`DigimarcId= 404407,32,,,4`

## 참조 {#section-75d4d2afd1df4127b31b1a82f30079d8}

[catalog::DigimarcInfo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-digimarcinfo-cat.md#reference-4925764ed683466bb7af4b807c86f8ba)
