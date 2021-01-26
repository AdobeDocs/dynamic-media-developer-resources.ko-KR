---
description: 경로 데이터를 포함합니다. 레이어 0 소스 이미지 파일의 Photoshop 경로를 응답 이미지에 포함할지 여부를 지정합니다.
seo-description: 경로 데이터를 포함합니다. 레이어 0 소스 이미지 파일의 Photoshop 경로를 응답 이미지에 포함할지 여부를 지정합니다.
seo-title: pathEmbed
solution: Experience Manager
title: pathEmbed
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 93e63c7c-c091-4bb1-baff-45706fd611ea
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 2%

---


# pathEmbed{#pathembed}

경로 데이터를 포함합니다. 레이어 0 소스 이미지 파일의 Photoshop 경로를 응답 이미지에 포함할지 여부를 지정합니다.

`pathEmbed=0|1`

## 속성 {#section-26eb1c9e13574a0eae39f6d5b92c8995}

요청 속성을 참조하십시오. 소스 이미지에 경로 데이터가 포함되어 있지 않으면 무시됩니다. 경로 데이터는 이미지 데이터처럼 크기가 조절되고 회전됩니다. `layer=0`의 소스 이미지의 경로만 처리됩니다.다른 레이어 이미지의 패스는 무시됩니다.

출력 이미지 형식이 경로 임베딩을 지원하지 않는 경우 무시됩니다. 경로 임베딩을 지원하는 출력 이미지 형식 목록은 `fmt=`의 설명을 참조하십시오.

## 제한 사항 {#section-697cddb79a1542bc8457d2f4f59eec69}

현재 닫힌 루프를 형성하지 않는 패스 열린 Photoshop 경로는 응답 이미지에 임베드할 수 없습니다.

## 기본값 {#section-62f113ad71c04517a2741d93319a2b5d}

`pathEmbed=0`를 선택합니다.

## 참조 {#section-9c20adb4147e45758ab109a543cc5862}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
