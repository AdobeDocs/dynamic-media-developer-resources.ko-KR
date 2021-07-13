---
description: 경로 데이터를 포함합니다. 레이어 0 소스 이미지 파일의 Photoshop 경로를 응답 이미지에 포함할지 여부를 지정합니다.
solution: Experience Manager
title: pathEmbed
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a3b305eb-0313-4c58-bd47-4f87e09d0e0b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 2%

---

# pathEmbed{#pathembed}

경로 데이터를 포함합니다. 레이어 0 소스 이미지 파일의 Photoshop 경로를 응답 이미지에 포함할지 여부를 지정합니다.

`pathEmbed=0|1`

## 속성 {#section-26eb1c9e13574a0eae39f6d5b92c8995}

요청 속성입니다. 소스 이미지에 경로 데이터가 포함되지 않은 경우 무시됩니다. 경로 데이터의 크기가 이미지 데이터처럼 조정되고 회전합니다. `layer=0` 소스 이미지의 경로만 처리됩니다. 다른 레이어 이미지의 경로는 무시됩니다.

출력 이미지 형식이 경로 포함을 지원하지 않는 경우에는 무시됩니다. 경로 포함을 지원하는 출력 이미지 형식 목록은 `fmt=`에 대한 설명을 참조하십시오.

## 제한 사항 {#section-697cddb79a1542bc8457d2f4f59eec69}

현재 열린 Photoshop 경로(닫힌 루프를 형성하지 않는 경로)는 응답 이미지에 포함할 수 없습니다.

## 기본값 {#section-62f113ad71c04517a2741d93319a2b5d}

`pathEmbed=0`를 사용하도록 선택할 수 있습니다.

## 참조 {#section-9c20adb4147e45758ab109a543cc5862}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
