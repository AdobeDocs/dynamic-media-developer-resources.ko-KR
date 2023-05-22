---
description: 응답 이미지 크기 제한. 클라이언트로 반환할 수 있는 응답 이미지의 최대 너비 및 높이입니다.
solution: Experience Manager
title: MaxPix
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0fd990cf-a54f-4574-8328-8988368d5875
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 3%

---

# MaxPix{#maxpix}

응답 이미지 크기 제한. 클라이언트로 반환할 수 있는 응답 이미지의 최대 너비 및 높이입니다.

요청으로 인해 너비 또는 높이가 보다 큰 응답 이미지가 반환되면 서버에서 오류를 반환합니다 `attribute::MaxPix`.

## 속성 {#section-b175425b9e9f48e0b1a71640f6a9e936}

0보다 큰 두 개의 정수를 쉼표로 구분합니다. 폭 및 높이(픽셀 단위). 를 로 설정할 수도 있습니다. `0,0` 응답 이미지 크기를 제한 없이 허용합니다.

## 기본값 {#section-1003537434da432fb2af100ecdbf9d72}

상속 위치 `default::MaxPix` 정의되지 않은 경우 또는 비어 있는 경우.

## 참조 {#section-7385697a1b86482bba19db894f7af95b}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)
