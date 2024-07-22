---
title: pathEmbed
description: 경로 데이터를 포함합니다. 레이어 0 소스 이미지 파일의 Photoshop 경로를 응답 이미지에 포함할지 여부를 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a3b305eb-0313-4c58-bd47-4f87e09d0e0b
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 2%

---

# pathEmbed{#pathembed}

경로 데이터를 포함합니다. 레이어 0 소스 이미지 파일의 Photoshop 경로를 응답 이미지에 포함할지 여부를 지정합니다.

`pathEmbed=0|1`

## 속성 {#section-26eb1c9e13574a0eae39f6d5b92c8995}

요청 속성입니다. 소스 이미지에 경로 데이터가 포함되지 않은 경우 무시됩니다. 경로 데이터는 이미지 데이터처럼 크기가 조정되고 회전됩니다. `layer=0`의 원본 이미지의 경로만 처리됩니다. 다른 레이어 이미지의 경로는 무시됩니다.

출력 이미지 형식이 경로 포함을 지원하지 않는 경우에는 무시됩니다. 경로 포함을 지원하는 출력 이미지 형식 목록을 보려면 `fmt=`의 설명을 참조하십시오.

## 제한 사항 {#section-697cddb79a1542bc8457d2f4f59eec69}

현재 Photoshop 경로 열기(닫힌 루프를 형성하지 않는 경로)는 응답 이미지에 포함할 수 없습니다.

## 기본값 {#section-62f113ad71c04517a2741d93319a2b5d}

`pathEmbed=0`(출력 이미지에 경로를 포함하지 않음)

## 참조 {#section-9c20adb4147e45758ab109a543cc5862}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
