---
description: 회신 이미지 크기 제한. 클라이언트에 반환될 수 있는 최대 회신 이미지 폭과 높이입니다.
solution: Experience Manager
title: MaxPix
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 0fd990cf-a54f-4574-8328-8988368d5875
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 3%

---

# MaxPix{#maxpix}

회신 이미지 크기 제한. 클라이언트에 반환될 수 있는 최대 회신 이미지 폭과 높이입니다.

요청에서 너비나 높이가 `attribute::MaxPix`보다 큰 응답 이미지가 발생하는 경우 서버에서 오류를 반환합니다.

## 속성 {#section-b175425b9e9f48e0b1a71640f6a9e936}

0보다 큰 두 정수(쉼표로 구분) 너비와 높이(픽셀 단위)입니다. 제한 없이 회신 이미지 크기를 허용하기 위해 `0,0`로 설정할 수도 있습니다.

## 기본값 {#section-1003537434da432fb2af100ecdbf9d72}

정의되지 않았거나 비어 있는 경우 `default::MaxPix`에서 상속됩니다.

## 참조 {#section-7385697a1b86482bba19db894f7af95b}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)
